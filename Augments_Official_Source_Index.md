# ARAM Mayhem Augments - Official Source Index

整理日期：2026-07-13

当前官网基线：Patch 26.13。Riot 官网截至本次采集没有提供“当前全部海克斯池 + 完整 tooltip”的单页数据库。本文只记录 Riot 官网补丁说明和开发者文章可直接确认的内容；未公开完整文本的条目必须标记为“待客户端/Wiki 补全文本”。

---

# 1. Source Pages

| Source ID | Riot official page | Date | Use |
|---|---|---:|---|
| RIOT-25.21 | https://www.leagueoflegends.com/en-us/news/game-updates/patch-25-21-notes/ | 2025-10-21 | ARAM Mayhem 上线定义 |
| RIOT-25.22 | https://www.leagueoflegends.com/en-us/news/game-updates/patch-25-22-notes/ | 2025-11-04 | 第一批 Mayhem augment 调整 |
| RIOT-25.23 | https://www.leagueoflegends.com/en-us/news/game-updates/patch-25-23-notes/ | 2025-11-18 | Mayhem augment 调整与系统调整 |
| RIOT-25.24 | https://www.leagueoflegends.com/en-us/news/game-updates/patch-25-24-notes/ | 2025-12-02 | 新增 Prismatic augment 与完整效果文本 |
| RIOT-26.3 | https://www.leagueoflegends.com/en-gb/news/game-updates/patch-26-3-notes/ | 2026-02-04 | 45 个新增/进度轨道/旧 Augment Sets |
| RIOT-26.8 | https://www.leagueoflegends.com/en-us/news/game-updates/league-of-legends-patch-26-8-notes/ | 2026-04-14 | Mayhem item/system 调整 |
| RIOT-26.9 | https://www.leagueoflegends.com/en-us/news/game-updates/league-of-legends-patch-26-9-notes/ | 2026-04-28 | Mayhem augment 调整 |
| RIOT-26.10 | https://www.leagueoflegends.com/en-us/news/game-updates/league-of-legends-patch-26-10-notes/ | 2026-05-12 | Mayhem augment QoL/bugfix |
| RIOT-26.11 | https://www.leagueoflegends.com/en-us/news/game-updates/league-of-legends-patch-26-11-notes/ | 2026-05-27 | Mayhem champion/bugfix，无新增 augment |
| RIOT-26.12 | https://www.leagueoflegends.com/en-us/news/game-updates/league-of-legends-patch-26-12-notes/ | 2026-06-09 | 当前大改：Ability/Quest Augments，移除 Trait System |
| RIOT-26.13 | https://www.leagueoflegends.com/en-us/news/game-updates/league-of-legends-patch-26-13-notes/ | 2026-06-23 | 当前基线调整 |
| RIOT-DEV-ARAM-MAYHEM | https://www.leagueoflegends.com/en-us/news/dev/dev-augmentmaxxing-aram-mayhem/ | 2026 | Ability/Quest Augment 设计说明 |

---

# 2. System Facts

| Fact | Official source | Status |
|---|---|---|
| ARAM Mayhem 是带 augments 的 5v5 单线模式。玩家在开局选择 1 个 augment，并在 7/11/15 级再次选择。 | RIOT-25.21 | Official confirmed |
| 26.12 新增 Ability Augments。Ability Augments 会直接升级英雄某个技能，只会提供当前英雄可用的技能强化。 | RIOT-26.12 | Official confirmed |
| 26.12 新增新版 Quest Augments。Quest Augments 会随特定目标完成而成长，可多阶段进化。 | RIOT-26.12 | Official confirmed |
| 一个 augment 可以同时是 Ability Augment 和 Quest Augment。 | RIOT-26.12 | Official confirmed |
| 26.12 移除 Trait System，并把部分 Trait 奖励转为独立 augments。 | RIOT-26.12 | Official confirmed |
| 26.13 后当前官网基线仍是 26.13；未发现 Riot 官网发布 26.14 正式补丁页。 | RIOT-26.13 / website search 2026-07-13 | Official-source checked |

---

# 3. Current 26.13 Officially Confirmed New/Converted Pool

这些条目来自 RIOT-26.12 “New Augments”和 Trait System 转换说明，并叠加 RIOT-26.13 的 tier/数值调整。多数条目官网只给名称和 tier，不给完整 tooltip。

## 3.1 Silver

| English name | Tier at 26.13 | Source | Official text status | Current status |
|---|---|---|---|---|
| Adaptive Ward | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Don't Change the Channel | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Double Defense | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Forged By The Master | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| It's Go Time | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Pursuit of Power | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Quest: Support Main | Silver | RIOT-26.12 | Partial design text | Current pool confirmed by Riot |
| Siphon | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Snowday | Silver | RIOT-26.12 | Converted trait reward; old set effect available from RIOT-26.3 | Current pool confirmed by Riot |
| Stackosaurus Rex | Silver | RIOT-26.12 | Converted trait reward; old set effect available from RIOT-26.3 | Current pool confirmed by Riot |
| Stay Resolute | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Trusty Weapon | Silver | RIOT-26.12 | Name only | Current pool confirmed by Riot |

## 3.2 Gold

| English name | Tier at 26.13 | Source | Official text status | Current status |
|---|---|---|---|---|
| BONK! | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Combusting Interest | Gold | RIOT-26.12 / RIOT-26.13 | 26.13: Percent Gold from Damage 1% to 0.75% | Current pool confirmed by Riot |
| Endless Decimation | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| From Downtown / From Down Town | Gold | RIOT-26.12 / RIOT-26.13 | 26.13 added restrictions to largest AoE size | Current pool confirmed by Riot |
| Hide on Bush | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Lil' Extra Help | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Mercy's Strike | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Nature is Healing | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Our Healing | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Overextender | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Pat On The Back | Gold | RIOT-26.12 / RIOT-26.13 | 26.13 bugfix: two players could create infinite shields | Current pool confirmed by Riot |
| Porcupine | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Pressure Cooker | Gold | RIOT-26.12 / RIOT-26.13 | Total Burn Damage 2% max Health to 1.5% max Health | Current pool confirmed by Riot |
| Pursuit of Haste | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Quickstep | Gold | RIOT-26.12 / RIOT-26.13 | Ability Augment; Prismatic to Gold in 26.13 | Current pool confirmed by Riot |
| Ravenous Bind | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Rejuvenation | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Shark Bait | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Shark Tempest | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Snowblast | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Terrain'd | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Tooth Fairy | Gold | RIOT-26.12 / RIOT-26.13 | Quest design partial; 26.13 Burst Threshold 20% to 25%, Lethality/Magic Pen 5 to 4 | Current pool confirmed by Riot |
| Void Dash | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Warlock Juicebox | Gold | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Wee Woo Wee Woo | Gold | RIOT-26.12 | Converted trait reward; old set effect available from RIOT-26.3 | Current pool confirmed by Riot |
| Yowch, My Coins! / Youch My Coins | Gold | RIOT-26.12 / RIOT-26.13 | Converted from Make it Rain; Coin Drops 16 to 9 in 26.13 | Current pool confirmed by Riot |

## 3.3 Prismatic

| English name | Tier at 26.13 | Source | Official text status | Current status |
|---|---|---|---|---|
| Archmage | Prismatic | RIOT-26.12 / RIOT-26.13 | Converted trait reward; Gold to Prismatic in 26.13 | Current pool confirmed by Riot |
| Chain Reaction | Prismatic | RIOT-26.12 / RIOT-DEV-ARAM-MAYHEM | Partial design text | Current pool confirmed by Riot |
| Dimension Shift | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| DropBear | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Echo Cast | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| En Passant | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Hellbent | Prismatic | RIOT-26.12 | Partial design: stack high enough to revive | Current pool confirmed by Riot |
| High Roller | Prismatic | RIOT-26.12 | Converted trait reward; old set effect available from RIOT-26.3 | Current pool confirmed by Riot |
| Multishot | Prismatic | RIOT-26.12 / RIOT-DEV-ARAM-MAYHEM | Partial design text | Current pool confirmed by Riot |
| One Trick Pony | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Overloaded | Prismatic | RIOT-26.12 | Ability Augment, name only in patch list | Current pool confirmed by Riot |
| Pin Cushion | Prismatic | RIOT-26.12 / RIOT-26.13 | Damage per Nail 20-30 to 20-60 | Current pool confirmed by Riot |
| Poro Stampede | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Rite of Ascension | Prismatic | RIOT-26.12 | Partial design: takedowns refresh cooldowns and heal | Current pool confirmed by Riot |
| Spellsplit | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Spirit Bomb | Prismatic | RIOT-26.12 / RIOT-26.13 | Shield Duration 4s to 2s | Current pool confirmed by Riot |
| Squishy Slappy Grab | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Surge Field | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Terror | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Titan's Resolve | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |
| Tripleshot | Prismatic | RIOT-26.12 | Name only | Current pool confirmed by Riot |

---

# 4. Older Officially Referenced Augments Still Requiring Current-Pool Verification

这些条目在 25.21-26.11 的官网补丁中作为 Mayhem augments 出现过，但 26.12 大改移除了部分旧条目并重构系统。除非在第 3 节中已被 26.12/26.13 再次确认，否则当前可用性必须用客户端/Wiki 复核。

| English name | Earliest/major official source | Official text or change captured | 26.13 current status |
|---|---|---|---|
| Big Brain | RIOT-26.10 | NEW: Refresh on Respawn or every 70 seconds | Needs current-pool verification |
| Blunt Force | RIOT-25.23 | AD 15% to 20% | Needs current-pool verification |
| Bounce of the Poro King | RIOT-26.3 | Progression reward; bounce as Poro King to knockback/deal damage | Needs current-pool verification |
| Cerberus | RIOT-25.24 / RIOT-26.12 | Gain Hail of Blades and Press the Attack; removed in 26.12 | Removed by Riot in 26.12 |
| Crack Open That Egg | RIOT-26.3 / RIOT-26.12 | Shields can detonate; removed in 26.12 | Removed by Riot in 26.12 |
| Donation | RIOT-26.3 | Gain significant Gold | Needs current-pool verification |
| Dropkick | RIOT-26.3 / RIOT-26.10 | Attacks execute low-health champions, restore health, knock back; bugfix in 26.10 | Needs current-pool verification |
| Earthwake | RIOT-25.24 | Full text captured: dash/blink trail detonates; limit 2 players per game | Needs current-pool verification |
| Empowered By The Faith | RIOT-26.3 | Heal/shield allies to earn Devotion; low-health execute | Needs current-pool verification |
| Fan the Hammer | RIOT-26.3 / RIOT-26.10 | Firecracker set member; no longer triggers on minions in 26.10 | Needs current-pool verification |
| Gash | RIOT-25.23 / RIOT-26.12 | Gain 50% Attack Speed; removed in 26.12 | Removed by Riot in 26.12 |
| Goldrend | RIOT-26.3 | Gold per proc 15 to 30 | Needs current-pool verification |
| Grandma Chili Oil / Grandma's Chili Oil | RIOT-26.9 / RIOT-26.12 | Burn/heal numbers adjusted; removed in 26.12 | Removed by Riot in 26.12 |
| Growth Spurt | RIOT-26.3 | Progression reward; active increases size/health and knocks up nearby enemies | Needs current-pool verification |
| Inferno Triggered | RIOT-26.3 | Automatically cast Samira R at S style | Needs current-pool verification |
| Laser Heal | RIOT-25.22 / RIOT-26.12 | Beam width/heal/damage adjusted; removed in 26.12 | Removed by Riot in 26.12 |
| Lightning Strike / Lightning Strikes | RIOT-25.23 / RIOT-26.3 / RIOT-26.12 | Attack Speed Requirement 4 to 3.5 to 1.75; removed in 26.12 | Removed by Riot in 26.12 |
| Lesser Heal | RIOT-26.3 | Cooldown 45 to 30; base heal 150-430 to 200-550 | Needs current-pool verification |
| Mystic Punch | RIOT-26.3 | On-hit ability cooldown reduction 20% to 1.25 seconds | Needs current-pool verification |
| Orbital Laser | RIOT-25.24 | Full text captured: replaces non-Flash summoner; 25% max health true damage plus magic damage over time; limit 1 player per game | Needs current-pool verification |
| Outlaw's Grit | RIOT-26.10 | Stacks reset based on 15s duration; shows on buff bar | Needs current-pool verification |
| Pandora's Box | RIOT-25.24 | Transmute all augments into random Prismatic augments | Needs current-pool verification |
| Protein Shake | RIOT-25.23 | Heal/shield power and resistance conversion buffed | Needs current-pool verification |
| Prom Queen | RIOT-26.9 | Cooldown 25s to 35s | Needs current-pool verification |
| Red Envelope | RIOT-26.3 / RIOT-26.12 | Progression reward; removed in 26.12 | Removed by Riot in 26.12 |
| Repulsor | RIOT-25.23 / RIOT-26.12 | Low-health knockback/slow; removed in 26.12 | Removed by Riot in 26.12 |
| Restless Restoration | RIOT-25.22 / RIOT-26.12 | Heal scaling adjusted; removed in 26.12 | Removed by Riot in 26.12 |
| Self Destruct | RIOT-25.23 / RIOT-26.12 | NEW bomb every 25s; removed in 26.12 | Removed by Riot in 26.12 |
| Shrink Engine | RIOT-26.3 | Progression reward; AH/MS/Shrink on takedown | Needs current-pool verification |
| Slow and Steady | RIOT-25.22 / RIOT-26.12 | AD formula adjusted; removed in 26.12 | Removed by Riot in 26.12 |
| Snowball Roulette | RIOT-25.22 / RIOT-25.23 / RIOT-26.12 | Random summoner spell effects; removed in 26.12 | Removed by Riot in 26.12 |
| Sonata | RIOT-26.3 | Progression reward; automatically alternate Sona E and W | Needs current-pool verification |
| Speed Demon | RIOT-26.3 / RIOT-26.12 | Movement speed reward; removed in 26.12 | Removed by Riot in 26.12 |
| Steel Your Heart / Quest: Steel Your Heart | RIOT-25.23 / RIOT-26.12 | Stack requirement 350 to 300; older Quest updated with clearer UI in 26.12 | Current as Quest family, exact pool/text needs verification |
| Stuck in Here with Me | RIOT-26.3 | Progression reward; after ultimate gain damage reduction and taunt enemies | Needs current-pool verification |
| Swift and Safe | RIOT-25.22 | Shield duration/amount adjusted | Needs current-pool verification |
| Tap Dancer | RIOT-25.22 / RIOT-26.3 | Buff can stack on minions/monsters; old Stackosaurus set member | Needs current-pool verification |
| Trueshot Prodigy | RIOT-25.24 / RIOT-26.12 | Long-range damage casts Ezreal R; removed in 26.12 | Removed by Riot in 26.12 |
| Ultimate Awakening | RIOT-25.22 / RIOT-25.24 | Reworked: ultimate AH, after ult reset basic ability cooldowns and gain 300 basic ability haste | Needs current-pool verification |
| Upgrade Collector | RIOT-25.22 / RIOT-26.13 Arena section | Execution threshold changes; Arena/Mayhem context differs | Needs current-pool verification |
| Upgrade Cutlass | RIOT-25.22 / RIOT-26.12 | Damage amp buffed; removed in 26.12 | Removed by Riot in 26.12 |
| Upgrade Mikael's Blessing | RIOT-25.22 / RIOT-26.12 | Now gives Mikael's Blessing or gold; removed in 26.12 | Removed by Riot in 26.12 |
| Upgrade Snowball / Snowball Upgrade | RIOT-26.3 / RIOT-26.10 | Snowday set member; bugfix around Snowball kill trigger | Needs current-pool verification |
| Upgrade Sword of Blossoming Dawn | RIOT-26.9 | Removed basic attack 50% damage penalty | Needs current-pool verification |
| Upgrade Thornmail | RIOT-26.3 / RIOT-26.12 | Progression reward; removed in 26.12 | Removed by Riot in 26.12 |
| Upgrade Zhonya's | RIOT-26.10 | NEW: grants 50% bonus MS during Stasis | Needs current-pool verification |
| Urf's Champion / Quest: Urf's Champion | RIOT-25.23 / RIOT-26.12 | Takedowns required 22 to 18; old Quest called out in 26.12 | Current as Quest family, exact pool/text needs verification |
| Veil of Warding | RIOT-25.22 | Cooldown 15 to 30 | Needs current-pool verification |
| Void Immolation / Quest: Void Immolation | RIOT-26.3 / RIOT-26.13 | Converts Sunfire/Hollow Radiance; 26.13 adds Desolate on-kill burst | Current pool confirmed by 26.13 adjustment; exact current name/tier needs verification |
| Weighted Popoffs | RIOT-26.3 / RIOT-26.12 | Progression reward; removed in 26.12 | Removed by Riot in 26.12 |

---

# 5. Removed By Riot in 26.12

These should not be used as current 26.13 recommendations unless a later source reintroduces them.

| Removed augment | Source |
|---|---|
| ??? | RIOT-26.12 |
| Buff Buddies | RIOT-26.12 |
| Cerberus | RIOT-26.12 |
| Cheating | RIOT-26.12 |
| Crack Open That Egg | RIOT-26.12 |
| Demon's Dance | RIOT-26.12 |
| Executioner | RIOT-26.12 |
| Feel the Burn | RIOT-26.12 |
| Frost Wraith | RIOT-26.12 |
| Gash | RIOT-26.12 |
| Grandma Chili Oil | RIOT-26.12 |
| Hat on a Hat | RIOT-26.12 |
| Holy Fire | RIOT-26.12 |
| im a baby kitty | RIOT-26.12 |
| Keystone Conjurer | RIOT-26.12 |
| Laser Heal | RIOT-26.12 |
| Lightning Strikes | RIOT-26.12 |
| Poro Blaster | RIOT-26.12 |
| Poro King | RIOT-26.12 |
| Rabble Rousing | RIOT-26.12 |
| Red Envelopes | RIOT-26.12 |
| Repulsor | RIOT-26.12 |
| Restless Restoration | RIOT-26.12 |
| Self Destruct | RIOT-26.12 |
| Slow and Steady | RIOT-26.12 |
| Snowball Roulette | RIOT-26.12 |
| Speed Demon | RIOT-26.12 |
| The Brutalizer | RIOT-26.12 |
| Tormentor | RIOT-26.12 |
| Trailblazer | RIOT-26.12 |
| Trueshot Prodigy | RIOT-26.12 |
| Twice Thrice | RIOT-26.12 |
| Upgrade Cutlass | RIOT-26.12 |
| Upgrade Hubris | RIOT-26.12 |
| Upgrade Mikaels | RIOT-26.12 |
| Upgrade Thornmail | RIOT-26.12 |
| Void Rift | RIOT-26.12 |
| Watch Out! Cupcake! | RIOT-26.12 |
| Weighted Popoffs | RIOT-26.12 |
| Wind beneath blade | RIOT-26.12 |

---

# 6. Legacy 26.3 Augment Sets

26.12 removed Trait System, so these set bonuses are historical. They remain useful for provenance because several current standalone augments were converted from these rewards.

| Legacy set | Official set effect / members | Current use |
|---|---|---|
| Deathknell | Set theme: death/true damage. Members: Clown College, Train of the Dead, Self Destruct, Dive Bomber. | Historical only unless individual augment is re-confirmed |
| Firecracker | Missiles bounce extra times. Members: Fan the Hammer, Magic Missile, Critical Missile, Light'em Up, Typhoon, Twin Fire. | Historical; Twin Fire/Twinfire later adjusted in 26.13 |
| High Roller | Minions can drop Stat Anvils; higher tiers improve Gold/Prismatic chance. | Converted to standalone Prismatic in 26.12 |
| Stackasaurus Rex | Gain more permanent stacks. Members include Infinite Recursion, Master of Duality, Tap Dancer, Soul Eater, Quest: Steal your heart, Phenomenal Evil, Shrink Engine, Hubris, Slap Around. | Converted to standalone Silver in 26.12 |
| Wee Woo Wee Woo | Speed plus Heal/Shield Power. Members include Windspeaker's Blessing, I'm a Baby Kitty Where is Mama, Upgrade: Mikaels Blessing, All For You, Critical Healing, Sonata, First Aid Kit. | Converted to standalone Gold in 26.12 |
| Fully Automated | Reduce autocast cooldowns; autocast cooldown scales with Ability Haste. Members include Prom Queen, Quantum Computing, Ok Boomerang, Sonata, Divine Intervention, Self Destruct, Frost Wraith, Firefox. | Historical only unless individual augment is re-confirmed |
| Archmage | Refund a random ability cooldown when casting a spell. Members: Overflow, Mind to Matter, Buff Buddy, Juiced, Ocean Soul. | Converted to standalone; Prismatic in 26.13 |
| Make it Rain | More gold from augments and kills. Members: Goldrend, Heads Up Cupcake!, Donation, Red Envelope, From Beginning to End, Upgrade Immolate, Upgrade Collector. | Converted to Yowch, My Coins! in 26.12 |
| Snowday | Snowball haste and extra snowball damage. Members: Biggest Snowball, Golden Snowball, Snowball Upgrade, Pinball Snowball, Snowball Roulette. | Converted to standalone Silver in 26.12 |

---

# 7. Data Quality Rules For Later Queries

| Field | Meaning |
|---|---|
| Current pool confirmed by Riot | Riot 26.12/26.13 explicitly lists or adjusts the augment after the 26.12 system reset. |
| Removed by Riot in 26.12 | Riot explicitly removed the augment in 26.12. |
| Needs current-pool verification | Riot mentioned the augment historically, but no post-26.12 source confirms current availability. |
| Name only | Riot provides only name/tier; no complete tooltip in official patch text. |
| Partial design text | Riot describes fantasy/core behavior but not complete in-client tooltip. |
| Full text captured | Riot patch note includes a usable effect description and/or numbers. |

Next required non-official-official-client step:

1. Extract current client tooltip strings from live client data or screenshot.
2. Cross-check with League Wiki/community database only as Tier C source.
3. Add official CN names from CN client, not direct translation.
4. Build machine-readable table: `english_name`, `official_cn`, `tier`, `augment_type`, `current_status`, `tooltip`, `source_id`, `patch_first_seen`, `patch_last_changed`, `confidence`.
