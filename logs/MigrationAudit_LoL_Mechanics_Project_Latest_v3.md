# Migration Audit: LoL_Mechanics_Project_Latest_v3

审计日期：2026-07-13

来源目录：`E:\github\tmp\LoL_Mechanics_Project_Latest_v3`

目的：检查旧外部聊天/导出目录中是否有未迁移但对当前项目有价值的内容。

---

# High Value Migrated

## Ability Class / Spell Hero Framework

来源：

- `Skill_v9_SpellHero_Framework.md`
- `Roadmap_v7_Update.md`

处理：

- 已迁入 `skill/AbilityClass.md`

价值：

- 当前 `Roadmap.md` 已提到 Ability Class，但缺具体分类和分析流程；
- 该框架决定英雄研究入口，避免所有英雄都套 On-Hit 模型。

## On-Hit Pool / Producer / Consumer / Hit vs Apply

来源：

- `Skill_v6_OnHitPool_Model.md`
- `Skill_v7_Hit_vs_ApplyOnHit.md`
- `Skill_v8_OnHit_Research_Standard.md`
- `LoL_Arena_机制分析_Skill_v2.md`

处理：

- 已迁入 `skill/OnHitModel.md`

价值：

- 当前项目已有 `ApplyCount.md`，但缺上游模型；
- Producer / Consumer 和 On-Hit Effects Pool 是后续 Mystic Punch、Ethereal Weapon、Dusk and Dawn 实验的基础。

## Mechanics Glossary Additions

来源：

- `Glossary_v5_Mechanics_Glossary.md`
- `Glossary_v2_EventTerminology.md`

处理：

- 已补入 `TERMINOLOGY.md`

价值：

- 当前 `TERMINOLOGY.md` 只有命名规范；
- 需要补齐 Attack、Hit、On-Hit、Apply On-Hit、On-Attack、Spellblade 等机制术语。

---

# Already Covered

## Data Collection Protocol

来源：

- `Data_Collection_Protocol_v1.md`

当前覆盖：

- `CONTRIBUTING.md`
- `DataAcquisition_Plan.md`
- `standards/Evidence.md`
- `standards/ConfidenceSystem.md`

结论：

- 核心采集规范已迁移并扩展，不需要整篇重复搬入。

## Official ARAM Mayhem Augments DB v0.1

来源：

- `LoL_ARAM_Mayhem_Augments_Official_DB_v0.1.md`

当前覆盖：

- `augments/OfficialSourceIndex.md`
- `augments/Database.md`
- `augments/HistoricalDatabase.md`
- `augments/AramMayhem_AlignedDatabase.md`

结论：

- 官方源和海克斯数据已由当前项目更细分的文档覆盖；
- 不建议整篇导入旧版数据库，避免回退到旧结构。

## Templates / Logs / Standards

来源：

- `Hero_Archive_Template_v2.md`
- `Experiment_Template_v1.md`
- `Evidence_v1.md`
- `Confidence_System_v1.md`
- `Open_Questions_v1.md`
- `Changelog_v1.md`
- `Research_Log_v1.md`

当前覆盖：

- `heroes/_HeroTemplate.md`
- `experiments/_Template.md`
- `standards/`
- `logs/`

结论：

- 已覆盖；可后续按需增强模板字段，但不需要原样搬。

---

# Not Migrated

## Old Roadmap Versions

来源：

- `LoL_Arena_机制研究计划_Roadmap_v1.md` 到 `Roadmap_v6.md`
- `Roadmap_v7_Update.md`

处理：

- 仅迁移 v7 的 Ability Class 方向；
- 其他路线图已被当前 `Roadmap.md` 吸收。

## Old Glossary Versions

来源：

- `Glossary_v1.md` 到 `Glossary_v4_Arena_Hextech_Naming.md`

处理：

- 当前 `TERMINOLOGY.md` 已覆盖 v4 命名规范；
- 只补 v5 机制术语。

---

# Follow-Up

- 把 `skill/OnHitModel.md` 中的实验编号落到 `experiments/` 具体模板；
- 基于 `skill/AbilityClass.md` 扩展 `heroes/_HeroTemplate.md` 的 Ability Class 字段；
- 用 `augments/AramMayhem_AlignedData.csv` 标记哪些海克斯属于 On-Hit、Spellblade、Cooldown、Buff/Debuff、Quest、Ability Augment。
