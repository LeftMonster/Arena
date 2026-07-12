# LoL Arena Mechanism Engine

这是一个围绕《英雄联盟》ARAM: Mayhem / Arena-style Augments 建立的机制研究库。

目标不是整理“什么最强”，而是长期回答：

> 游戏内部是如何结算的？

项目采用 Evidence First + Event Tree First 的方式维护数据。每条结论都必须能追溯到来源、版本、可信度和实验状态。

---

# Directory Map

| Path | Purpose |
|---|---|
| `PROJECT_HANDOFF.md` | 给 Codex/Agent 的启动说明和当前最高优先级 |
| `CONTRIBUTING.md` | 数据采集、可信度、实验记录规范 |
| `SOURCES.md` | 官方来源入口和资料优先级 |
| `TERMINOLOGY.md` | 中英术语、官方中文名、历史俗称统一 |
| `Roadmap.md` | 当前研究路线 |
| `skill/` | 机制模型，例如 Event Tree、Apply Count、Ability Class |
| `heroes/` | 英雄档案与英雄级机制分析 |
| `augments/` | 海克斯数据库、Ability/Quest Augments、补丁历史 |
| `experiments/` | 实验记录与实验模板 |
| `standards/` | 可信度体系、证据模板等通用标准 |
| `logs/` | 研究日志、开放问题、版本日志 |

---

# Current Priority

最高优先级是补齐 ARAM: Mayhem 当前海克斯数据库：

1. Riot 官网来源已落档到 `augments/OfficialSourceIndex.md`。
2. 当前主数据库在 `augments/Database.md`。
3. 下一步需要补正式服客户端 tooltip、国服官方中文名、Ability Augment 英雄技能映射。

---

# Research Order

默认研究顺序：

Ability Class → Ability Augments → Quest Augments → Event Tree → Normal Augments → Items → Interactions → Experiments → Hero Archive

不要从 build 推荐直接开始。
