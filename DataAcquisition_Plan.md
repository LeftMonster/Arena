# Data Acquisition Plan

整理日期：2026-07-13

目标：为 ARAM: Mayhem / Arena-style Augments 的数据采集建立分层方案。优先使用稳定、可复现、低干扰的数据源；只有在必要时才升级到真机浏览器/去特征自动化浏览器采集。

---

# 1. Acquisition Layers

## Layer 1: Official Web Sources

用途：

- 确认系统变更；
- 确认新增/移除；
- 确认 Riot 明确公开的效果和数值；
- 建立 patch provenance。

来源：

- Riot Patch Notes
- Riot Dev Blog
- Riot 官方公告

限制：

- Riot 官网没有当前完整海克斯池 + 完整 tooltip 的单页数据库；
- 很多条目只有名称和 tier；
- 不能补完整客户端文案。

当前状态：

- 已建立 `augments/OfficialSourceIndex.md`。

---

## Layer 2: Static Client Mirrors / Extracted Data

用途：

- 获取客户端名称；
- 获取本地化文本；
- 获取客户端 ID、rarity、icon、internal name；
- 发现官网未列出的候选条目。

来源：

- CommunityDragon
- CDragon raw files
- 后续可能加入 DataDragon / Meraki / League Wiki 交叉验证

中文二级来源：

- 中文 Wiki / 数据站 / 攻略站 / 社区帖可作为补充检索层；
- 使用精确中文名、英文名、NameId 组合检索；
- 详细策略见 `ChineseSecondarySources_Plan.md`。

当前状态：

- 已使用 CDragon `cherry-augments.json` 匹配 58/59 个当前池中文名；
- 已发现 18 个 CDragon 候选项，需判断是历史残留、重命名还是漏收。

限制：

- CDragon 是客户端镜像/社区数据，不等同 Riot 官网；
- tooltip 可能由运行时变量拼接；
- 可能包含历史残留、其他模式或未启用内容；
- rarity 可能与 Riot patch note 存在差异，需要复核。

---

## Layer 3: Live Client / Real Browser Collection

用途：

- 当静态文件无法还原 tooltip；
- 当网页有 JS 渲染、反爬、登录、地区化或动态接口；
- 当需要实机截图、录屏、客户端内实际展示文案；
- 当需要确认当前池是否真实可选。

可用方案：

- 用户提供的去爬虫特征自动化浏览器；
- 真机浏览器手动/半自动采集；
- Playwright / Selenium / CDP 连接到已启动浏览器；
- 截图 + OCR / DOM 抓取 / 网络日志抓取。

使用原则：

1. 只有 Layer 1 / Layer 2 不足时再启用。
2. 优先只读采集，不做破坏性操作。
3. 每次采集记录浏览器、地区、客户端版本、账号环境、时间。
4. 截图/HTML/JSON 原始材料要保存到后续 `evidence/` 或 `data_sources/` 快照目录。
5. 抓到的结果仍需标注来源，不直接混成 Riot 官网事实。

触发条件：

- CDragon tooltip 缺失或全是变量占位；
- 某个 augment 在 Riot 官网和 CDragon rarity/status 冲突；
- 需要确认 `One Trick Pony` 这类官网有、CDragon 未匹配条目；
- 需要确认 CDragon 18 个候选是否当前可用；
- 需要国服客户端官方中文 tooltip。

---

# 2. Current Augment Completeness Status

当前我们拥有：

- Riot 26.12/26.13 官网确认池：59 个；
- CDragon 中文名匹配：58/59 个；
- Riot 26.12 明确移除：40 个；
- 历史出现但当前需复核：31 个；
- CDragon 候选但未收入当前 59：18 个。

重要边界：

> 59 个不是“已经证明的当前全部海克斯池”，而是“Riot 官网 26.12/26.13 已确认的当前池基线”。

原因：

1. Riot 官网没有完整当前池列表。
2. CDragon 存在额外候选和历史残留。
3. Ability Augments 可能有英雄技能映射变体。
4. 客户端实际池需要正式服实机或完整客户端数据确认。

当前判断：

- 59 个可以作为当前研究基线；
- 不能宣布它们就是全部；
- 下一步必须做客户端 tooltip / 当前池复核。

---

# 3. Next Verification Tasks

## Task A: Resolve Current 59

目标：

- 补完 59 个的中文 tooltip；
- 解决 `One Trick Pony` 未匹配问题；
- 解决 `Pursuit of Power`、`Terror` rarity 冲突；
- 确认 `Double Defense` 是否等于 CDragon `Bolstered / 加固护盾`。

推荐路径：

1. 继续解析 CDragon stringtable / spell modifier 数据；
2. 若仍缺失，使用真机浏览器或正式服客户端截图采集；
3. 把截图/原始文本作为证据保存。

## Task B: Verify 18 CDragon Candidates

目标：

- 判断是否漏收；
- 判断是否历史残留；
- 判断是否重命名/合并；
- 必要时迁移到 `Database.md` 或 `HistoricalDatabase.md`。

## Task C: Build Machine-readable Table

建议字段：

```text
english_name
official_cn
tier
client_rarity
augment_type
current_status
tooltip_cn
tooltip_en
source_primary
source_secondary
patch_first_seen
patch_last_changed
confidence
needs_review
notes
```

---

# 4. Browser Collection Notes

如果启用用户提供的真机/去特征自动化浏览器，建议采集策略：

1. 打开正式服客户端或网页来源；
2. 固定地区和语言，例如 zh_CN；
3. 逐条采集 augment 面板：
   - 名称；
   - 等级；
   - tooltip；
   - 图标；
   - 是否可选；
   - 英雄/技能映射条件；
4. 保存：
   - screenshot；
   - DOM/HTML；
   - network log；
   - browser/client version；
   - timestamp。

安全约束：

- 不进行批量登录尝试；
- 不进行对战内影响他人的自动操作，除非明确需要实验；
- 只采集公开显示/自己账号可见数据；
- 保留原始证据，不只保存整理后的结论。
