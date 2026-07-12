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
