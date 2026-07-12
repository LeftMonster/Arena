# Chinese Secondary Sources Plan

整理日期：2026-07-13

目标：在 Riot 官网和客户端/CDragon 数据之外，利用中文语料补充海克斯效果说明、发现漏收条目，并作为二级/三级交叉验证来源。

---

# 1. Source Position

中文网页、攻略站、社区帖、视频文案、中文 Wiki / 数据站可以使用，但定位必须清楚：

| Source type | Tier | Use |
|---|---|---|
| Riot 国服官网 / 客户端中文文本 | Tier A/B | 官方中文名、官方 tooltip、补丁说明 |
| CDragon zh_cn 客户端数据 | Tier B/C | 客户端中文名、内部 ID、rarity、候选条目 |
| 中文 Wiki / 维护型数据库 | Tier C | 补效果描述、查历史条目、辅助 current pool 判断 |
| 中文攻略站 / 论坛 / 视频文字 | Tier D | 发现线索、发现俗称、发现疑似漏收 |
| 个人猜测 / 未标来源搬运 | Tier E | 只能作为检索线索，不进结论 |

原则：

- 中文二级来源不能覆盖 Riot 官网和正式服客户端。
- 中文二级来源可以帮助解释 CDragon 字段、补效果描述、发现漏收候选。
- 每条来自中文二级来源的效果都必须保留 URL、抓取日期、页面标题和置信等级。

---

# 2. Search Strategy

不要只用泛词搜索：

- `海克斯大乱斗 强化符文 大全`
- `英雄联盟 海克斯大乱斗 符文`

这类搜索噪音很高，容易命中普通符文、其他游戏、维基通用页。

推荐使用精准组合：

```text
"中文名" "海克斯大乱斗"
"中文名" "强化符文"
"中文名" "ARAM"
"英文名" "海克斯大乱斗"
"CDragon NameId" "lol"
"augmentNameId" "cherry"
```

示例：

```text
"自适应防护" "海克斯大乱斗"
"牙仙子" "海克斯大乱斗"
"超负荷" "瑞兹" "海克斯大乱斗"
"DoubleDefense" "cherry"
```

---

# 3. Current Findings

已尝试泛搜和部分精准中文搜索：

- `海克斯大乱斗 强化符文 自适应防护 效果`
- `海克斯大乱斗 强化符文 大全 牙仙子 快步 大法师`
- `英雄联盟 海克斯大乱斗 强化符文 效果 列表`
- `自适应防护 英雄联盟 强化符文`
- `牙仙子 LOL 海克斯大乱斗`

结果：

- 泛搜质量较差；
- 搜索结果大量命中普通“符文”、其他游戏、维基通用条目；
- 目前未发现可直接作为完整当前池数据库的中文维护页。

结论：

- 中文语料应作为补充检索层；
- 主体数据仍需 Riot 官网 + 客户端/CDragon + 必要时真机浏览器采集。

---

# 4. Workflow

## Step 1: Build Query List

从 `augments/CurrentAugments_CN_Effects.md` 提取：

- 英文名；
- 中文名；
- CDragon ID；
- NameId；
- CDragon rarity。

为每个条目生成 3-5 个查询。

## Step 2: Search And Classify

每个命中页面分类：

| Classification | Meaning |
|---|---|
| UsefulEffect | 有完整效果描述 |
| UsefulNameOnly | 只确认中文名/英文名 |
| UsefulPatch | 有补丁变化 |
| CandidatePool | 提供当前池列表或候选列表 |
| LowQuality | 搬运、无来源、过期、不清楚版本 |
| Irrelevant | 非本模式或非 LoL |

## Step 3: Extract Evidence

每条有效来源记录：

```text
augment
source_url
source_title
source_type
retrieved_at
claimed_patch
effect_text
confidence
notes
```

## Step 4: Cross-check

进入主库前必须满足：

1. Riot 官网或客户端确认当前存在；
2. CDragon / 客户端名可匹配；
3. 中文来源效果不与官方补丁冲突；
4. 若冲突，标记为 `needs_review`。

---

# 5. Priority Targets

优先中文复核这些问题条目：

| Target | Reason |
|---|---|
| One Trick Pony | Riot 官网确认，但 CDragon 名称未匹配 |
| Pursuit of Power / 威能之追求 | Riot tier 与 CDragon rarity 冲突 |
| Terror / 惊惧 | Riot tier 与 CDragon rarity 冲突 |
| Double Defense / 加固护盾 | 需确认是否对应 Bolstered |
| CDragon 18 candidates | 判断历史残留、重命名或漏收 |

---

# 6. Use With Real Browser

如果中文站点有反爬、JS 渲染、登录态或搜索结果不稳定：

- 可使用用户提供的去爬虫特征真机浏览器；
- 优先保存 HTML、截图和网络日志；
- 不只保存整理后的文本；
- 采集记录写入 `logs/ResearchLog.md`。

详细浏览器采集方案见：

- `DataAcquisition_Plan.md`
