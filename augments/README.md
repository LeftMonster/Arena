# Augments

本目录存放 ARAM: Mayhem / Arena-style Augments 数据。

| File | Purpose |
|---|---|
| `Database.md` | 当前主数据库，人类可读版 |
| `CurrentAugments_CN_Effects.md` | 当前 59 个官网确认海克斯的中文名、简要效果和 CDragon 对照 |
| `CandidateReview.md` | CDragon 候选、未匹配项、rarity 冲突项的复核表 |
| `HistoricalDatabase.md` | 历史海克斯库：已移除、旧版本、待复核、转换来源 |
| `OfficialSourceIndex.md` | Riot 官网来源索引 |
| `AbilityAugments.md` | Ability Augments 专用索引 |
| `QuestAugments.md` | Quest Augments 专用索引 |
| `PatchHistory.md` | 海克斯补丁历史 |

当前最高优先级：

1. 补齐全部当前海克斯；
2. 补正式服客户端 tooltip；
3. 补国服官方中文名；
4. 标注 source、patch、confidence、current_status。

当前完整性边界：

- Riot 官网确认当前基线：59 个；
- 这 59 个不是已证明的“全部当前池”；
- 还需要用客户端 tooltip、CDragon 候选和必要时真机浏览器采集来复核完整性；
- 详细采集策略见根目录 `DataAcquisition_Plan.md`。

查询规则：

- 当前版本分析优先读 `Database.md`。
- 历史来源、旧视频/旧攻略对照、已移除条目读 `HistoricalDatabase.md`。
- 官网原始采集依据读 `OfficialSourceIndex.md`。
- 中文名和 CDragon 客户端对照读 `CurrentAugments_CN_Effects.md`。
- CDragon 候选和冲突项复核读 `CandidateReview.md`。
