# Augment Candidate Review

整理日期：2026-07-13

用途：复核 CDragon 中存在、但未收入当前 Riot 59 条官网确认池的候选条目。这里的条目不能直接视为当前可用，需要继续通过 Riot patch、客户端实机、中文二级来源或 Wiki 复核。

---

# 1. Current Problem Items

| Item | Finding | Next step |
|---|---|---|
| One Trick Pony | Riot 26.12 官网列为 Prismatic，但 CDragon `cherry-augments.json` 和 stringtable 精确搜索未命中。 | 用客户端实机/真机浏览器确认是否存在，或查是否改名。 |
| Pursuit of Power / 威能之追求 | CDragon ID 2116 `SpecializedEmpowerment`，中文名可匹配；CDragon rarity = Gold，Riot 26.12 表中为 Silver。 | 以正式服客户端实际显示或后续 patch 为准。 |
| Terror / 惊惧 | CDragon ID 2065 `ARAM_Terror`，中文名可匹配；CDragon rarity = Gold，Riot 26.12 表中为 Prismatic。 | 以正式服客户端实际显示或后续 patch 为准。 |
| Double Defense / 加固护盾 | CDragon ID 2144 `DoubleDefense`，英文客户端名为 `Bolstered`，中文名为 `加固护盾`。 | 基本可对应 Double Defense，但需确认 Riot patch 名称是否旧名/内部名差异。 |

---

# 2. CDragon Candidates Outside Current Riot 59

| English | 中文名 | CDragon ID | rarity | NameId | Initial classification | Reason |
|---|---|---:|---|---|---|---|
| Heads Up Cupcake! | 当心小蛋糕！ | 2001 | kPrismatic | ARAM_WatchOutGrapefruit | LikelyRemovedOrRenamed | 与 26.12 removed `Watch Out! Cupcake!` 名称接近。 |
| Void Rift | 虚空裂隙 | 2002 | kPrismatic | ARAM_VoidRift | RemovedOrHistorical | Riot 26.12 明确移除 `Void Rift`。 |
| Bounce of the Poro King | 魄罗之王的弹跳 | 2003 | kPrismatic | ARAM_PoroKing | LegacyUnverified | Riot 26.3 历史 progression reward，当前需复核。 |
| Empowered By The Faithful | 信念者的强化 | 2004 | kPrismatic | ARAM_EmpoweredByTheFaithful | NeedsReview | 可能对应历史 `Empowered By The Faith`，当前需复核。 |
| Triggered Inferno | 扳机炼狱 | 2005 | kPrismatic | ARAM_InfernoTriggered | NeedsReview | 可能对应历史 `Inferno Triggered`，当前需复核。 |
| Dropkick | 飞身踢 | 2006 | kPrismatic | ARAM_Dropkick | LegacyUnverified | Riot 26.3/26.10 历史出现，当前需复核。 |
| Devil on Your Shoulder | 你肩上的恶魔 | 2007 | kPrismatic | ARAM_LittleDevil | NeedsReview | CDragon 候选，当前来源不足。 |
| Weighted Popoffs | 负重爆气 | 2008 | kSilver | ARAM_WeightedPopoffs | RemovedOrHistorical | Riot 26.12 明确移除。 |
| Zealot | 狂热者 | 2009 | kSilver | ARAM_Zealot | NeedsReview | CDragon 候选，当前来源不足。 |
| Double Tap | 双发快射 | 2010 | kGold | ARAM_DoubleTap | NeedsReview | CDragon 候选，当前来源不足。 |
| Juiced | 注魔 | 2016 | kSilver | ARAM_Juiced | NeedsReview | 旧 Archmage set member，当前需复核。 |
| Purist - Caster | 纯粹主义者 - 术师 | 2018 | kSilver | ARAM_Purist_Caster | NeedsReview | CDragon 候选，当前来源不足。 |
| Crit 'n Cast | 由暴生急 | 2024 | kSilver | CritNCast | NeedsReview | CDragon 候选，当前来源不足。 |
| Kill Secured | 杀意翻涌 | 2026 | kSilver | KillSecured | NeedsReview | CDragon 候选，当前来源不足。 |
| Snap Back | 复位 | 2109 | kGold | SnapBack | NeedsReview | CDragon 候选，当前来源不足。 |
| Ult Bot | 大招工具人 | 2118 | kPrismatic | SkipTheBasics | NeedsReview | CDragon 候选，当前来源不足。 |
| Reload | 装填 | 2126 | kGold | KeepGoing | NeedsReview | CDragon 候选，当前来源不足。 |
| Double Strike | 双重打击 | 2148 | kSilver | DoubleStrike | NeedsReview | CDragon 候选，当前来源不足。 |

---

# 3. Review Workflow

1. 精确中文检索：`"中文名" "海克斯大乱斗"`、`"中文名" "强化符文"`。
2. 精确英文/NameId 检索：`"NameId" "cherry"`、`"English" "ARAM Mayhem"`。
3. 查 Riot 后续 patch 是否重新引入或调整。
4. 查正式服客户端实际池/tooltip。
5. 如果网页或客户端采集受限，按 `DataAcquisition_Plan.md` 使用真机浏览器/去特征化自动化浏览器。
