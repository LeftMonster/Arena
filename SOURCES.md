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
