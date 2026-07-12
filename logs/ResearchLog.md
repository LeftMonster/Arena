# Research Log

用于记录每日研究进度。

格式：

日期： 研究主题： 资料来源： 结论： 新增开放问题： 需要实验：
知识库是否更新：

---

日期：2026-07-13

研究主题：Riot 官网 ARAM Mayhem Augments 官方源采集

资料来源：

- Riot Patch 25.21 / 25.22 / 25.23 / 25.24
- Riot Patch 26.3 / 26.8 / 26.9 / 26.10 / 26.11 / 26.12 / 26.13
- Riot dev article: Augmentmaxxing ARAM: Mayhem

结论：

- Riot 官网没有当前完整海克斯池与完整 tooltip 单页；
- 26.12 是当前资料的关键 reset 点：新增 Ability/Quest Augments，移除 Trait System，并移除一批旧 augment；
- 已建立 `augments/OfficialSourceIndex.md`，用于区分当前 Riot 确认池、已移除池、历史出现但当前需复核池。

新增开放问题：

- 当前正式服客户端是否存在官网未列出的旧普通海克斯；
- 26.12 新增 Ability Augments 的每英雄技能映射；
- 国服官方中文名称完整表。

需要实验：

- 暂无，当前是资料采集阶段；下一步应先补客户端文本。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：核心数据源登记补齐

资料来源：

- https://www.leagueoflegends.com/en-us/news/
- https://arammayhem.com/augments/
- https://communitydragon.org/
- https://wiki.leagueoflegends.com/en-us/

结论：

- 已将 Riot Games Official News / Patch Notes / Dev Blog 登记为 Tier A 第一数据源；
- 已将 ARAM Mayhem Augments Database 登记为 Tier C maintained community database；
- arammayhem.com/augments 页面声称当前共有 199 个强化符文，分布为 69 棱彩、74 金色、56 银色，并显示已移除 56；
- 已将 CommunityDragon 登记为 Tier B/C client mirror；
- 已将 League Wiki 登记为 Tier C maintained community wiki；
- 当前 59 个 Riot 官网确认基线需要与 arammayhem 199 当前池做完整差异对比。

新增开放问题：

- arammayhem 199 当前池与 Riot 官网 59 基线的差异列表；
- arammayhem 的完整效果文本、中文名、统计字段是否可稳定抓取；
- arammayhem 的数据来源和更新机制。

需要实验：

- 暂无。下一步是抓取 arammayhem 当前池列表并与 CDragon / Riot 基线对齐。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：未匹配与 CDragon 候选复核

资料来源：

- CommunityDragon `cherry-augments.json`
- CommunityDragon zh_cn `cherry-augments.json`
- CommunityDragon en_us / zh_cn `lol.stringtable.json`
- 当前 `augments/CurrentAugments_CN_Effects.md`

结论：

- `Double Defense` 基本可对应 CDragon `DoubleDefense / Bolstered / 加固护盾`；
- `Pursuit of Power / 威能之追求` 中文名和 CDragon ID 可确认，但 rarity 与 Riot 26.12 不一致；
- `Terror / 惊惧` 中文名和 CDragon ID 可确认，但 rarity 与 Riot 26.12 不一致；
- `One Trick Pony` 在 CDragon 名称表和 stringtable 精确搜索中仍未命中；
- 已新增 `augments/CandidateReview.md` 记录 18 个候选项的初步分类。

新增开放问题：

- `One Trick Pony` 是否已改名、被客户端隐藏，或 Riot 官网列表与当前客户端不一致；
- 候选项中哪些是当前可用，哪些只是历史残留。

需要实验：

- 需要正式服客户端实际池/tooltip 采集；若采集受限，可启用真机/去特征化浏览器方案。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：中文二级来源检索策略

资料来源：

- 用户建议；
- 当前中文搜索尝试；
- `augments/CurrentAugments_CN_Effects.md` 中的中文名和 CDragon NameId。

结论：

- 中文语料可以作为二级/三级数据源，用于补效果说明、发现漏收条目和核对俗称；
- 泛搜噪音较高，容易命中普通符文、其他游戏或过期内容；
- 更适合基于客户端中文名、英文名、NameId 做精确检索；
- 已新增 `ChineseSecondarySources_Plan.md`。

新增开放问题：

- 是否存在高质量中文维护页覆盖当前 ARAM: Mayhem augment 池；
- CDragon 18 个候选中是否有中文社区确认当前可用的条目。

需要实验：

- 无。下一步是按优先目标逐条中文精确检索。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：真机浏览器采集策略纳入计划

资料来源：

- 当前 Riot 官网和 CDragon 采集结果；
- 用户说明可提供去爬虫特征自动化浏览器。

结论：

- 当前 59 个是 Riot 官网确认基线，不是已证明的完整当前池；
- CDragon 已提供中文名和候选条目，但 tooltip 和当前池完整性仍需复核；
- 已新增 `DataAcquisition_Plan.md`，把真机浏览器/去特征自动化浏览器列为 Layer 3 采集方案；
- 触发条件包括 tooltip 缺失、网页/接口限制、rarity/status 冲突、官网有但 CDragon 未匹配、候选漏收复核。

新增开放问题：

- 是否需要用户提供可自动化浏览器环境来采集正式服客户端 tooltip；
- 59 个之外的 CDragon 候选是否有当前可用条目。

需要实验：

- 暂无，下一步是客户端数据复核和 tooltip 采集。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：当前海克斯中文名与候选漏收项检索

资料来源：

- `augments/OfficialSourceIndex.md`
- CommunityDragon `cherry-augments.json` English / zh_cn
- CommunityDragon `game/zh_cn/data/menu/en_us/lol.stringtable.json`

结论：

- 已新增 `augments/CurrentAugments_CN_Effects.md`；
- 当前 Riot 59 个官网确认条目中，58 个匹配到 CDragon 中文客户端名；
- `One Trick Pony` 暂未在 CDragon 名称表中直接匹配；
- 发现 18 个 CDragon `id 2000-2149` 范围内、但不在当前 Riot 59 条中的候选，后续需要判断是历史残留、重命名还是漏收。

新增开放问题：

- `Pursuit of Power`：Riot 26.12 列为 Silver，但 CDragon rarity 显示 Gold；
- `Terror`：Riot 26.12 列为 Prismatic，但 CDragon rarity 显示 Gold；
- `Double Defense` 是否对应 CDragon 的 `Bolstered / 加固护盾`；
- `One Trick Pony` 的客户端名称和 ID；
- CDragon 候选 18 条中哪些实际仍在当前池内。

需要实验：

- 暂无。下一步优先做客户端 tooltip 解析/实机截图复核。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：Meraki lolstaticdata 数据源评估

资料来源：

- https://github.com/meraki-analytics/lolstaticdata
- Meraki CDN champions/items JSON 入口说明

结论：

- Meraki lolstaticdata 对英雄技能和物品结构化数据有帮助；
- 不适合作为海克斯当前池/官方 tooltip 主数据源；
- 建议作为 Tier C community structured source 纳入，辅助 Event Tree、Hero Archive、装备机制研究。

新增开放问题：

- Meraki 当前 JSON 是否覆盖 Arena/ARAM Mayhem 特殊物品；
- champions JSON 字段是否足够支持 Ability Class 自动候选分类；
- 是否需要建立快照缓存以避免 `latest` 漂移。

需要实验：

- 先用 Master Yi、Gangplank、Corki 三个英雄做字段质量验证。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：历史海克斯数据库拆分

资料来源：

- `augments/OfficialSourceIndex.md`
- Riot 26.12 Removed Augments
- Riot 25.21-26.13 Mayhem 相关补丁记录

结论：

- 已新增 `augments/HistoricalDatabase.md`；
- 将历史条目分为 Removed、LegacyUnverified、Removed with historical detail、Converted/Provenance、Legacy Trait Sets；
- 当前主库 `augments/Database.md` 继续作为当前版本分析入口，历史条目不混入主库。

新增开放问题：

- LegacyUnverified 条目中哪些仍在当前正式服池内；
- Void Immolation / Quest: Void Immolation、Twin Fire / Twinfire 等疑似改名或合并条目的当前客户端名。

需要实验：

- 无。下一步应先做客户端 tooltip/当前池采集。

知识库是否更新：是。

---

日期：2026-07-13

研究主题：项目文档架构重组

资料来源：

- 用户提供的 `架构说明.txt` 参考结构；
- 当前项目已有 Markdown 文档。

结论：

- 根目录保留项目入口、规范、资料源、术语和路线图；
- 机制模型迁移到 `skill/`；
- 海克斯数据库和官网源索引迁移到 `augments/`；
- 英雄模板迁移到 `heroes/`；
- 实验模板迁移到 `experiments/`；
- 可信度和证据规则迁移到 `standards/`；
- 日志、开放问题、版本日志迁移到 `logs/`。

新增开放问题：

- 是否需要把当前文档进一步拆成机器可读 CSV/JSON。

需要实验：

- 无。

知识库是否更新：是。
