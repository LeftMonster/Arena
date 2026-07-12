# Sources

资料优先级：

1. Riot official sources
2. Riot patch notes
3. Riot developer blogs
4. Official client text / screenshots
5. Community League Wiki / maintained databases
6. Experiments
7. Theory

社区资料只能作为补充来源，不能覆盖 Riot 官方事实。理论必须明确标记，不得和官方结论混写。

---

# Current Official Source Index

ARAM: Mayhem 海克斯官网采集索引：

- `augments/OfficialSourceIndex.md`

该索引记录：

- Riot 25.21-26.13 中出现过的 Mayhem augment 相关条目；
- 26.13 当前 Riot 官网确认池；
- 26.12 明确移除池；
- 历史出现但当前需客户端复核的条目；
- 每个条目的官方文本完整度。

---

# Registered Data Sources

## Riot Games Official News / Patch Notes / Dev Blog

URL:

- https://www.leagueoflegends.com/en-us/news/

Tier:

- Tier A

Use:

- 官方补丁说明；
- 官方开发者文章；
- 系统机制、增删改、版本变更；
- 当前所有结论的最高优先级来源。

Notes:

- 这是第一数据源；
- 若 Riot 与社区/客户端镜像冲突，优先保留 Riot 说法，并标记客户端差异待复核。

## ARAM Mayhem Augments Database

URL:

- https://arammayhem.com/augments/
- https://arammayhem.com/zh-cn/augments/

Tier:

- Tier C maintained community database

Use:

- 当前海克斯池完整性复核；
- 中文名/英文名对照；
- 胜率、登场率、顶级英雄等统计；
- 已移除条目和历史条目对照；
- 和 CDragon / Riot 官网交叉验证漏收项。

Current observation:

- 页面声称 ARAM: Mayhem 当前共有 199 个强化符文；
- 分布为 69 棱彩、74 金色、56 银色；
- 已移除 56；
- 数据更新时间显示为 7月10日。

Notes:

- 这是非常重要的当前池候选源，但不是 Riot 官方；
- 不能直接覆盖 Riot 官网或正式服客户端；
- 后续需要抓取其完整表格，与 `augments/CurrentAugments_CN_Effects.md` 和 CDragon 对齐。

## CommunityDragon

URL:

- https://communitydragon.org/
- https://raw.communitydragon.org/

Tier:

- Tier B/C client mirror

Use:

- 客户端静态数据；
- zh_cn 本地化名称；
- internal ID / NameId / rarity；
- 候选条目发现；
- 客户端 tooltip/stringtable 复核。

Current files used:

- `plugins/rcp-be-lol-game-data/global/default/v1/cherry-augments.json`
- `plugins/rcp-be-lol-game-data/global/zh_cn/v1/cherry-augments.json`
- `game/zh_cn/data/menu/en_us/lol.stringtable.json`

Notes:

- CDragon 是客户端数据镜像，不等同 Riot 官网；
- 可能包含历史残留、未启用内容、其他模式内容；
- 适合做客户端侧复核和候选发现。

## League Wiki

URL:

- https://wiki.leagueoflegends.com/en-us/

Tier:

- Tier C maintained community wiki

Use:

- 英雄技能机制；
- item / augment / mode 机制解释；
- 历史版本和 patch 追溯；
- 与 Meraki / CDragon / Riot patch 交叉验证。

Notes:

- 不能作为 Riot 官方事实；
- 适合作为机制解释、历史追溯和字段理解来源；
- 进入主库时必须保留页面 URL、版本信息和检索日期。

---

# Known Limitation

截至 2026-07-13，Riot 官网没有提供“当前全部海克斯池 + 完整 tooltip”的单页数据库。

后续需要从正式服客户端文本或维护数据库补齐：

- 完整 tooltip；
- 国服官方中文名；
- 当前 tier；
- Ability Augment 英雄技能映射；
- 当前是否仍在池内。

数据采集升级路线：

- `DataAcquisition_Plan.md`

当 Riot 官网、CDragon、静态文件不足以还原 tooltip 或当前池时，可以升级到正式服客户端/真机浏览器/去特征自动化浏览器采集，但采集结果必须保留原始证据和来源标记。

---

# Candidate Community Data Sources

## Chinese secondary sources

中文资料可以作为二级/三级交叉验证来源，尤其用于：

- 补中文效果描述；
- 发现漏收条目；
- 对照国服俗称和官方中文名；
- 查旧攻略/旧视频中的历史机制来源。

但中文攻略站、论坛、视频文案不能直接作为官方事实。详细策略：

- `ChineseSecondarySources_Plan.md`

## Meraki lolstaticdata

URL:

- https://github.com/meraki-analytics/lolstaticdata

本项目定位：

- Tier C community structured source；
- 适合 champion ability data 和 item data；
- 可辅助 `heroes/`、`skill/EventTree.md`、装备机制研究；
- 不作为 ARAM: Mayhem Augments 当前池或官方 tooltip 的主数据源。

详细接入计划：

- `DataSource_MerakiStaticData_Plan.md`
