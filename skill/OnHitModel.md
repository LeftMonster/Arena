# On-Hit Model

本文档保存 On-Hit Pool、Producer / Consumer、Hit vs Apply 的统一分析模型。

来源：

- 旧上下文 `LoL_Mechanics_Project_Latest_v3/Skill_v6_OnHitPool_Model.md`
- 旧上下文 `LoL_Mechanics_Project_Latest_v3/Skill_v7_Hit_vs_ApplyOnHit.md`
- 旧上下文 `LoL_Mechanics_Project_Latest_v3/Skill_v8_OnHit_Research_Standard.md`
- 旧上下文 `LoL_Mechanics_Project_Latest_v3/LoL_Arena_机制分析_Skill_v2.md`

---

# Core Distinctions

Hit、On-Hit、Apply On-Hit 不能混用。

| Term | Meaning |
|---|---|
| Hit | 命中事件。一次攻击或技能成功命中目标。 |
| On-Hit | 攻击特效本身，是效果，不是事件。 |
| On-Hit Effects Pool | 当前角色拥有的全部攻击特效集合。 |
| Apply On-Hit | 执行一轮攻击特效池，是事件/动作。 |
| Apply Count | 一次动作最终执行 Apply On-Hit 的总次数。 |

关键规则：

- 装备数量不等于 Apply Count；
- 一次 Apply On-Hit 会统一执行当前 On-Hit Effects Pool；
- 一个技能可以造成 Spell Damage，同时执行一轮或多轮 Apply On-Hit；
- 某些海克斯可能监听 Hit，另一些可能监听 Apply On-Hit，必须分开验证。

---

# On-Hit Effects Pool

On-Hit Effects Pool 表示当前角色拥有的全部攻击特效。

例子：

- Master Yi E true damage
- Blade of the Ruined King
- Wit's End
- Nashor's Tooth
- champion-specific on-hit effects
- augment-provided on-hit effects

一次 Apply On-Hit 会统一执行池中的全部效果。

示例：

```text
Apply On-Hit
↓
On-Hit Effects Pool
├─ Master Yi E
├─ Blade of the Ruined King
├─ Wit's End
└─ Nashor's Tooth
↓
Final Result
```

这仍然是一轮 Apply，不是四轮 Apply。

---

# Producer / Consumer

## Producer

Producer 负责向 On-Hit Effects Pool 添加攻击特效。

例子：

| Champion | Skill | Adds To Pool |
|---|---|---|
| Master Yi | E | true damage on-hit |
| Kassadin | W | W on-hit effect |
| Kayle | E | E on-hit effect |

Producer 不负责执行攻击特效。

## Consumer

Consumer 负责执行一轮 Apply On-Hit。

例子：

| Champion | Skill |
|---|---|
| Master Yi | Q |
| Gangplank | Q / Barrel path needs verification |
| Ezreal | Q |

Consumer 不创造攻击特效，它执行当前池。

---

# Recommended Event Tree

```text
Cast
↓
On-Attack (if any)
↓
Hit / Spell Hit
↓
Spell Damage
↓
Apply On-Hit (0..n)
↓
On-Hit Effects Pool
↓
Proc
↓
Buff / Debuff
↓
Final Damage / Final Result
```

---

# Analysis Procedure

分析任何攻击特效流派：

1. 识别 Producer：谁向 On-Hit Pool 添加效果？
2. 识别 Consumer：谁执行 Apply On-Hit？
3. 统计 Hit Count。
4. 统计 Apply Count。
5. 确认海克斯/装备监听 Hit、Apply、Spell Damage 还是 Proc。
6. 对每个关键交互设计实验。

禁止：

- 把 Hit 当作 Apply；
- 把 On-Hit 效果数量当作 Apply Count；
- 把项目模型写成 Riot 官方术语。

---

# Known Working Hypotheses

Mystic Punch：

- 更可能与 Apply On-Hit 次数存在关联，而不是与攻击特效装备数量关联；
- 仍需更多实测确认，不能写成官方结论。

Dusk and Dawn：

- 可能额外执行 Apply On-Hit；
- 是否作用于 Runaan's Hurricane 副箭、Dual Wield、Ethereal Weapon，需要实验。

Ethereal Weapon：

- 可能让技能获得额外 Apply On-Hit 路径；
- 需要逐英雄确认技能类型、目标数、倍率和内部冷却。

---

# Experiments

EXP-APPLY-001：

验证 Runaan's Hurricane 每支副箭是否都独立触发 Mystic Punch。

EXP-APPLY-002：

验证 Dusk and Dawn 额外 Apply 是否同样作用于 Hurricane 副箭。

EXP-APPLY-003：

验证 Dual Wield、Ethereal Weapon 加入后，Apply Count 是否继续累加。

EXP-YI-001：

验证 Master Yi Q 单目标多次命中时的 Apply On-Hit 执行次数、倍率、是否全部执行 On-Hit Pool。

EXP-YI-002：

分别测试 Master Yi E、Blade of the Ruined King、Wit's End、Nashor's Tooth 在 Q 中是否有不同 On-Hit 系数或特殊限制。

EXP-YI-003：

测试 Ethereal Weapon、Mystic Punch、Dusk and Dawn 与 Master Yi Q 的交互。

---

# Status

当前可信度：

- Master Yi E 为 On-Hit true damage：需以官方技能文本复核；
- Master Yi Q Apply On-Hit：需以官方技能文本复核；
- Producer / Consumer、On-Hit Effects Pool、Apply Count：项目内部分析模型；
- Dusk and Dawn、Mystic Punch、Ethereal Weapon 的复合交互：实验优先级高。
