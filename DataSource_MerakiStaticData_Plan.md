# Meraki lolstaticdata Data Source Plan

评估日期：2026-07-13

目标仓库：

- https://github.com/meraki-analytics/lolstaticdata

结论：可以纳入项目，但定位应是 **Champion / Item static data support source**，不是当前海克斯主数据源。

---

# 1. What This Source Provides

Meraki lolstaticdata 提供用于生成 League of Legends 静态数据的代码和 CDN JSON 数据。

仓库 README 明确说明：

- 主要目标是提供高质量 champion 和 item data；
- champion ability information 来自 League of Legends Wiki；
- Riot Data Dragon 的 champion ability 文本和数值经常不准确或难解析；
- Community Dragon 数据更接近客户端，但 champion ability 数据复杂、cryptic；
- Meraki 试图在准确性、可读性、可解析性之间取平衡；
- 数据可通过 CDN 获取：
  - `http://cdn.merakianalytics.com/riot/lol/resources/latest/en-US/champions.json`
  - `http://cdn.merakianalytics.com/riot/lol/resources/latest/en-US/items.json`

---

# 2. Fit For This Project

## Useful

Meraki 对本项目有价值，主要用于：

1. 英雄技能基础数据
   - 技能描述；
   - 技能数值；
   - AD/AP/HP 等 scaling；
   - 冷却、消耗、等级成长；
   - 技能标签初步推断。

2. 物品基础数据
   - 普通装备；
   - 可能包含部分 Arena/ARAM 相关物品，需验证；
   - 支撑装备与技能/海克斯交互分析。

3. Event Tree 建模辅助
   - 给 `heroes/` 档案提供技能文本和数值底稿；
   - 给 `skill/EventTree.md` 的事件拆分提供输入；
   - 给 `skill/ApplyCount.md` 的英雄技能案例提供基础信息。

4. Patch diff 辅助
   - 如果保存每个版本快照，可用于比较英雄技能/物品数值变化；
   - 不能替代 Riot patch notes，但可以作为结构化 diff 工具。

## Not Sufficient

Meraki 不应作为海克斯主数据源，原因：

1. README 自述范围主要是 champions 和 items。
2. 它不是 Riot 官方来源。
3. 它的 champion ability information 依赖 League Wiki。
4. 对 ARAM: Mayhem Augments / Ability Augments / Quest Augments 没有明确覆盖承诺。
5. 它无法确认当前 Mayhem augment pool、国服官方中文名、客户端 tooltip。

---

# 3. Source Tier

建议纳入当前项目资料体系：

| Data type | Tier | Use |
|---|---|---|
| Champion ability data | Tier C | Community maintained structured source; useful for parsing and cross-checking |
| Item data | Tier C | Community maintained structured source; useful for item database |
| Augment data | Not primary | Only use if later confirmed it contains relevant fields |
| Official facts | Not acceptable alone | Must cross-check with Riot official/client sources |

Meraki 数据进入知识库时必须保留来源字段：

- `source = Meraki lolstaticdata`
- `upstream = League Wiki / Meraki parser`
- `source_tier = Tier C`
- `retrieved_at`
- `game_patch` 或 CDN version path

---

# 4. Proposed Integration

## Phase 1: Metadata Registration

新增到 `SOURCES.md`：

- Meraki lolstaticdata
- 用途：champion / item structured data
- 等级：Tier C
- 限制：非 Riot 官方；不作为海克斯当前池判断依据

## Phase 2: Snapshot Storage

不要直接依赖 `latest` CDN 做长期研究。`latest` 会随版本漂移，无法复现旧结论。

建议后续建立：

```text
data_sources/
└── meraki/
    ├── README.md
    ├── snapshots/
    │   └── <patch>/
    │       ├── champions.json
    │       └── items.json
    └── scripts/
        └── fetch_meraki.py
```

每次采集必须记录：

- URL；
- retrieved_at；
- patch；
- sha256；
- file size；
- license / attribution note。

## Phase 3: Derived Tables

从 Meraki JSON 派生项目内部表，不直接手写进机制结论。

建议生成：

```text
derived/
├── champions/
│   ├── abilities_index.csv
│   ├── cooldowns.csv
│   ├── ratios.csv
│   └── tags_candidates.csv
└── items/
    ├── items_index.csv
    ├── active_items.csv
    ├── on_hit_candidates.csv
    └── spellblade_candidates.csv
```

## Phase 4: Cross-check Rules

任何从 Meraki 导出的机制结论必须至少满足：

1. Meraki structured data 给出候选；
2. Riot patch/client/wiki 至少一个来源确认文本；
3. 关键交互仍需实验验证；
4. 不把 Meraki 的推断字段写成 Riot 官方事实。

---

# 5. Immediate Use Cases

## Master Yi

用途：

- 读取 Q/E/R 的基础文本和数值；
- 标记 Q 是否包含 Apply On-Hit 相关描述；
- 和 `skill/ApplyCount.md` 的剑圣 Q 模型交叉验证。

## Gangplank

用途：

- 读取 Q/E Barrel 相关文本；
- 辅助判断 Barrel 是否应拆为 Spell Damage、On-Hit、Spellblade、Apply On-Hit 候选事件；
- 后续仍需实验验证 Barrel + Ethereal Weapon + Mystic Punch。

## Corki

用途：

- 读取被动、技能和攻击修饰信息；
- 支撑“Spellblade Hero，不是 generic On-Hit champion”的分类检查。

## Item Research

用途：

- 初步筛选 on-hit、spellblade、active item；
- 为后续装备数据库和 Event Tree 提供结构化输入。

---

# 6. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| CDN `latest` 漂移 | 旧结论不可复现 | 保存 patch snapshot 和 sha256 |
| 非官方数据 | 不能直接作为事实 | 标 Tier C，必须交叉验证 |
| Wiki/parser 错误 | 可能污染机制库 | 只作为候选，不作为最终结论 |
| 缺少 Mayhem augment 数据 | 不能补当前海克斯池 | 海克斯仍走 Riot 官网 + client tooltip |
| 特殊机制无法简单 JSON 表达 | Event Tree 可能误判 | 特殊交互单独建 case note 和实验 |

---

# 7. Decision

建议纳入，但范围限定：

- 接入：Yes
- 作为海克斯主数据源：No
- 作为英雄技能/物品结构化数据源：Yes
- 作为 Event Tree / Hero Archive 辅助源：Yes
- 作为官方事实来源：No

下一步：

1. 在 `SOURCES.md` 登记 Meraki；
2. 建立 `data_sources/meraki/README.md`；
3. 后续写 `fetch_meraki.py` 拉取 champions/items 快照；
4. 先用 Master Yi、Gangplank、Corki 做 3 个样例验证字段质量。
