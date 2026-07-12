# Historical Augments Database

整理日期：2026-07-13

用途：存放 ARAM: Mayhem / Arena-style Augments 的历史资料。这里的条目不能直接当作当前版本可用海克斯使用；当前分析和查询主库仍以 `Database.md` 为准。

---

# Status Rules

| Status | Meaning |
|---|---|
| Removed | Riot 明确在后续补丁中移除。 |
| LegacyUnverified | Riot 历史补丁中出现过，但 26.12 系统重置后当前是否仍在池内未确认。 |
| Converted | 旧 Trait / 旧奖励 / 旧海克斯机制被转成当前独立海克斯或新名字。 |
| RenamedOrMerged | 疑似改名、合并或转化，需要客户端/Wiki 复核。 |
| Reintroduced | 曾经移除后又由后续补丁确认回归。 |

---

# 1. Removed By Riot in 26.12

这些条目由 Riot 26.12 补丁明确列为 Removed Augments。除非后续补丁重新引入，否则不能作为当前可用池使用。

| English name | Status | Removed patch | Source | Notes |
|---|---|---|---|---|
| ??? | Removed | 26.12 | RIOT-26.12 | Name appears literally as `???`. |
| Buff Buddies | Removed | 26.12 | RIOT-26.12 | Related to old Archmage set as `Buff Buddy`. |
| Cerberus | Removed | 26.12 | RIOT-26.12 | Full 25.24 text existed; see Legacy section. |
| Cheating | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Crack Open That Egg | Removed | 26.12 | RIOT-26.12 | Historical progression/augment reference. |
| Demon's Dance | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Executioner | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Feel the Burn | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Frost Wraith | Removed | 26.12 | RIOT-26.12 | Old Fully Automated set member. |
| Gash | Removed | 26.12 | RIOT-26.12 | 25.23 added 50% Attack Speed. |
| Grandma Chili Oil | Removed | 26.12 | RIOT-26.12 | 26.9 adjusted burn/heal values. |
| Hat on a Hat | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Holy Fire | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| im a baby kitty | Removed | 26.12 | RIOT-26.12 | Old Wee Woo Wee Woo set member. |
| Keystone Conjurer | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Laser Heal | Removed | 26.12 | RIOT-26.12 | 25.22 adjusted beam width/heal/damage. |
| Lightning Strikes | Removed | 26.12 | RIOT-26.12 | Also seen as Lightning Strike. |
| Poro Blaster | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Poro King | Removed | 26.12 | RIOT-26.12 | Related to Poro King progression rewards. |
| Rabble Rousing | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Red Envelopes | Removed | 26.12 | RIOT-26.12 | 26.3 progression reward was Red Envelope Augment. |
| Repulsor | Removed | 26.12 | RIOT-26.12 | 25.23 added low-health knockback/slow. |
| Restless Restoration | Removed | 26.12 | RIOT-26.12 | 25.22 adjusted heal scaling. |
| Self Destruct | Removed | 26.12 | RIOT-26.12 | 25.23 added self bomb every 25s. |
| Slow and Steady | Removed | 26.12 | RIOT-26.12 | 25.22 adjusted AD formula. |
| Snowball Roulette | Removed | 26.12 | RIOT-26.12 | 25.23 reworked random summoner spell behavior. |
| Speed Demon | Removed | 26.12 | RIOT-26.12 | 26.3 progression reward. |
| The Brutalizer | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Tormentor | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Trailblazer | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Trueshot Prodigy | Removed | 26.12 | RIOT-26.12 | 25.24 full text existed. |
| Twice Thrice | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Upgrade Cutlass | Removed | 26.12 | RIOT-26.12 | 25.22 damage amp buffed. |
| Upgrade Hubris | Removed | 26.12 | RIOT-26.12 | Historical upgrade augment. |
| Upgrade Mikaels | Removed | 26.12 | RIOT-26.12 | Also appears as Upgrade Mikael's Blessing. |
| Upgrade Thornmail | Removed | 26.12 | RIOT-26.12 | 26.3 progression reward. |
| Void Rift | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |
| Watch Out! Cupcake! | Removed | 26.12 | RIOT-26.12 | Name overlaps old Make it Rain member `Heads Up Cupcake!`; verify before merging. |
| Weighted Popoffs | Removed | 26.12 | RIOT-26.12 | 26.3 progression reward. |
| Wind beneath blade | Removed | 26.12 | RIOT-26.12 | Historical Mayhem augment. |

Removed count: 40.

---

# 2. LegacyUnverified

这些条目在 25.21-26.11 Riot 官网补丁中出现过，但 26.12 系统重置后没有被 26.12/26.13 明确列为当前池。后续需要用正式服客户端文本或维护数据库确认。

| English name | Status | Official source | Historical text/change | Notes |
|---|---|---|---|---|
| Big Brain | LegacyUnverified | RIOT-26.10 | Refresh on Respawn or every 70 seconds. | Needs current-pool verification. |
| Blunt Force | LegacyUnverified | RIOT-25.23 | AD 15% to 20%. | Needs current-pool verification. |
| Bounce of the Poro King | LegacyUnverified | RIOT-26.3 | Progression reward; bounce as Poro King to knock back and deal damage. | Needs current-pool verification. |
| Donation | LegacyUnverified | RIOT-26.3 | Gain significant Gold. | Needs current-pool verification. |
| Dropkick | LegacyUnverified | RIOT-26.3 / RIOT-26.10 | Attacks execute low-health champions, restore health, knock back; 26.10 bugfix. | Needs current-pool verification. |
| Earthwake | LegacyUnverified | RIOT-25.24 | Dashing/blinking leaves detonating trail; 70% minion damage; limit 2 players per game. | Full historical text captured. |
| Empowered By The Faith | LegacyUnverified | RIOT-26.3 | Heal/shield allies to earn Devotion; low-health execute. | Needs current-pool verification. |
| Fan the Hammer | LegacyUnverified | RIOT-26.3 / RIOT-26.10 | Firecracker set member; 26.10 no longer triggers on minions. | Needs current-pool verification. |
| Goldrend | LegacyUnverified | RIOT-26.3 | Gold per proc 15 to 30. | Needs current-pool verification. |
| Growth Spurt | LegacyUnverified | RIOT-26.3 | Active increases size/health and knocks up nearby enemies. | Progression reward. |
| Inferno Triggered | LegacyUnverified | RIOT-26.3 | Automatically casts Samira R at S style. | Needs current-pool verification. |
| Lesser Heal | LegacyUnverified | RIOT-26.3 | Cooldown 45 to 30; base heal 150-430 to 200-550. | Needs current-pool verification. |
| Mystic Punch | LegacyUnverified | RIOT-26.3 | On-hit ability cooldown reduction changed from 20% to 1.25 seconds. | High research priority for Apply Count. |
| Orbital Laser | LegacyUnverified | RIOT-25.24 | Replaces non-Flash summoner; active deals 25% max Health true damage plus magic damage over 3s; limit 1 player per game. | Full historical text captured. |
| Outlaw's Grit | LegacyUnverified | RIOT-26.10 | Stacks reset based on a 15s duration and show on buff bar. | Needs current-pool verification. |
| Pandora's Box | LegacyUnverified | RIOT-25.24 | Transmute all augments into random Prismatic augments. | Needs current-pool verification. |
| Protein Shake | LegacyUnverified | RIOT-25.23 | Heal/shield power and resistance conversion buffed. | Needs current-pool verification. |
| Prom Queen | LegacyUnverified | RIOT-26.9 | Cooldown 25s to 35s. | Needs current-pool verification. |
| Shrink Engine | LegacyUnverified | RIOT-26.3 | AH/MS/Shrink on takedown. | Progression reward. |
| Sonata | LegacyUnverified | RIOT-26.3 | Automatically alternate Sona E and W. | Progression reward. |
| Steel Your Heart / Quest: Steel Your Heart | LegacyUnverified | RIOT-25.23 / RIOT-26.12 | Stack requirement 350 to 300; 26.12 calls out clearer Quest UI. | Current Quest family likely exists, exact current entry needs verification. |
| Stuck in Here with Me | LegacyUnverified | RIOT-26.3 | After ultimate gain damage reduction and taunt enemies. | Progression reward. |
| Swift and Safe | LegacyUnverified | RIOT-25.22 | Shield duration 3 to 2; shield amount reduced. | Needs current-pool verification. |
| Tap Dancer | LegacyUnverified | RIOT-25.22 / RIOT-26.3 | Buff can stack on minions/monsters; old Stackosaurus set member. | Needs current-pool verification. |
| Ultimate Awakening | LegacyUnverified | RIOT-25.22 / RIOT-25.24 | Reworked: gain ultimate AH; after ult reset basic cooldowns and gain 300 basic ability haste for 15s. | Needs current-pool verification. |
| Upgrade Collector | LegacyUnverified | RIOT-25.22 / RIOT-26.13 Arena section | Execution threshold changes; Arena/Mayhem context differs. | Needs mode-specific verification. |
| Upgrade Snowball / Snowball Upgrade | LegacyUnverified | RIOT-26.3 / RIOT-26.10 | Snowday set member; bugfix around Snowball kill trigger. | Needs current-pool verification. |
| Upgrade Sword of Blossoming Dawn | LegacyUnverified | RIOT-26.9 | Removed basic attack 50% damage penalty. | Needs current-pool verification. |
| Upgrade Zhonya's | LegacyUnverified | RIOT-26.10 | Grants 50% bonus MS during Stasis. | Needs current-pool verification. |
| Urf's Champion / Quest: Urf's Champion | LegacyUnverified | RIOT-25.23 / RIOT-26.12 | Takedowns required 22 to 18; 26.12 calls out old Quest examples. | Current Quest family likely exists, exact current entry needs verification. |
| Veil of Warding | LegacyUnverified | RIOT-25.22 | Cooldown 15 to 30. | Needs current-pool verification. |

LegacyUnverified count: 31.

---

# 3. Removed Entries With Historical Detail

这些条目同时出现在历史调整记录和 26.12 移除列表中。保留历史效果是为了以后追溯机制来源。

| English name | Status | Official source | Historical text/change |
|---|---|---|---|
| Cerberus | Removed | RIOT-25.24 / RIOT-26.12 | Gain Hail of Blades and Press the Attack. Hail of Blades grants first 3 attacks increased Attack Speed; Press the Attack bursts after 3 attacks and increases damage until leaving combat. |
| Crack Open That Egg | Removed | RIOT-26.3 / RIOT-26.12 | Shields can detonate; exact current tooltip not retained in Riot text here. |
| Gash | Removed | RIOT-25.23 / RIOT-26.12 | Additionally gain 50% Attack Speed. |
| Grandma Chili Oil / Grandma's Chili Oil | Removed | RIOT-26.9 / RIOT-26.12 | Base damage per second 100 to 150; bonus damage per burn source 60 to 50; heal values reduced. |
| Laser Heal | Removed | RIOT-25.22 / RIOT-26.12 | Beam width 175 to 215; heal and damage increased. |
| Lightning Strike / Lightning Strikes | Removed | RIOT-25.23 / RIOT-26.3 / RIOT-26.12 | Attack Speed requirement changed from 4 to 3.5, later to 1.75. |
| Red Envelope | Removed | RIOT-26.3 / RIOT-26.12 | Progression reward: pick up Red Envelopes to increase Gold and a random stat. |
| Repulsor | Removed | RIOT-25.23 / RIOT-26.12 | When dropping below 35% health, knock back enemies and slow them for 90% for 1.5s. |
| Restless Restoration | Removed | RIOT-25.22 / RIOT-26.12 | Heal scaling adjusted from +0.02% max Health to +0.01% max Health. |
| Self Destruct | Removed | RIOT-25.23 / RIOT-26.12 | Every 25 seconds, attach a bomb to yourself that explodes, damages, and knocks up enemies. |
| Slow and Steady | Removed | RIOT-25.22 / RIOT-26.12 | AD gained changed to 25 + 0.75 AD per 1% Attack Speed. |
| Snowball Roulette | Removed | RIOT-25.22 / RIOT-25.23 / RIOT-26.12 | Random harmful summoner spell on snowball hit; random beneficial spell on snowball dash. |
| Speed Demon | Removed | RIOT-26.3 / RIOT-26.12 | Progression reward: movement speed reward. |
| Trueshot Prodigy | Removed | RIOT-25.24 / RIOT-26.12 | Damaging enemies over 700 units away casts Ezreal R; 15s overall cooldown; limit 1 player per game. |
| Upgrade Cutlass | Removed | RIOT-25.22 / RIOT-26.12 | Damage amp 15% to 25%. |
| Upgrade Mikael's Blessing / Upgrade Mikaels | Removed | RIOT-25.22 / RIOT-26.12 | Gives Mikael's Blessing or gold if already owned; inventory handling noted. |
| Upgrade Thornmail | Removed | RIOT-26.3 / RIOT-26.12 | Progression reward. |
| Weighted Popoffs | Removed | RIOT-26.3 / RIOT-26.12 | Progression reward: striking enemies allows abilities to cooldown faster. |

---

# 4. Converted / Provenance

这些条目用于追踪当前海克斯的历史来源。当前可用性以 `Database.md` 为准。

| Current or historical name | Status | Converted / provenance notes | Source |
|---|---|---|---|
| Archmage | Converted | Old Trait Set: casting a spell refunded a random ability cooldown. 26.12 converted to standalone; 26.13 changed Gold to Prismatic. | RIOT-26.3 / RIOT-26.12 / RIOT-26.13 |
| High Roller | Converted | Old Trait Set: minions had chance to drop Stat Anvils; higher set tiers improved Gold/Prismatic chance. 26.12 converted to standalone Prismatic. | RIOT-26.3 / RIOT-26.12 |
| Snowday | Converted | Old Trait Set: Snowball Ability Haste and increased Snowball damage. 26.12 converted to standalone Silver. | RIOT-26.3 / RIOT-26.12 |
| Stackosaurus Rex / Stackasaurus Rex | Converted | Old Trait Set: gain more permanent stacks. 26.12 converted to standalone Silver; spelling differs between Riot references. | RIOT-26.3 / RIOT-26.12 |
| Wee Woo Wee Woo | Converted | Old Trait Set: speed plus heal/shield power. 26.12 converted to standalone Gold. | RIOT-26.3 / RIOT-26.12 |
| Yowch, My Coins! / Youch My Coins | Converted | Converted from Make it Rain; 26.13 coin drops 16 to 9. | RIOT-26.3 / RIOT-26.12 / RIOT-26.13 |
| Void Immolation / Quest: Void Immolation | RenamedOrMerged | 26.13 adjusted Quest: Void Immolation and Void Immolation. Current exact name/tier needs client verification. | RIOT-26.3 / RIOT-26.13 |
| Twin Fire / Twinfire | RenamedOrMerged | Old Firecracker member `Twin Fire`; 26.13 adjusts `Twinfire` critical chance 15% to 25%. Current exact name/tier needs client verification. | RIOT-26.3 / RIOT-26.13 |

---

# 5. Legacy 26.3 Trait Sets

26.12 移除了 Trait System，因此以下 set bonus 是历史资料。它们的价值是解释某些当前海克斯从哪里来。

| Legacy set | Status | Official set effect / members | Source |
|---|---|---|---|
| Deathknell | Removed system | Theme: death and true damage. Members: Clown College, Train of the Dead, Self Destruct, Dive Bomber. | RIOT-26.3 |
| Firecracker | Removed system | Missiles bounce extra times. Members: Fan the Hammer, Magic Missile, Critical Missile, Light'em Up, Typhoon, Twin Fire. | RIOT-26.3 |
| High Roller | Converted | Minions can drop Stat Anvils; higher set tiers improve Gold/Prismatic chance. | RIOT-26.3 |
| Stackasaurus Rex | Converted | Gain more permanent stacks. Members include Infinite Recursion, Master of Duality, Tap Dancer, Soul Eater, Quest: Steal your heart, Phenomenal Evil, Shrink Engine, Hubris, Slap Around. | RIOT-26.3 |
| Wee Woo Wee Woo | Converted | Speed plus Heal/Shield Power. Members include Windspeaker's Blessing, I'm a Baby Kitty Where is Mama, Upgrade: Mikaels Blessing, All For You, Critical Healing, Sonata, First Aid Kit. | RIOT-26.3 |
| Fully Automated | Removed system | Reduce autocast cooldowns; autocast cooldown scales with Ability Haste. Members include Prom Queen, Quantum Computing, Ok Boomerang, Sonata, Divine Intervention, Self Destruct, Frost Wraith, Firefox. | RIOT-26.3 |
| Archmage | Converted | Refund a random ability cooldown when casting a spell. Members: Overflow, Mind to Matter, Buff Buddy, Juiced, Ocean Soul. | RIOT-26.3 |
| Make it Rain | Converted | More gold from augments and kills. Members: Goldrend, Heads Up Cupcake!, Donation, Red Envelope, From Beginning to End, Upgrade Immolate, Upgrade Collector. | RIOT-26.3 |
| Snowday | Converted | Snowball haste and extra snowball damage. Members: Biggest Snowball, Golden Snowball, Snowball Upgrade, Pinball Snowball, Snowball Roulette. | RIOT-26.3 |

---

# 6. Maintenance Rules

1. 当前版本查询默认不要读本文件，先读 `Database.md`。
2. 遇到旧视频、旧攻略、旧 Wiki 文本时，用本文件判断是否是历史条目。
3. 如果正式服客户端确认某个 LegacyUnverified 条目仍可用，把它复制/迁移到 `Database.md`，并把本文件状态更新为 `Reintroduced` 或 `CurrentVerified`。
4. 如果发现 Riot 后续补丁明确回归旧条目，记录 `Reintroduced patch`。
5. 历史条目保留来源和补丁，不删除。
