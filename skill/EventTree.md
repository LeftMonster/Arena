# Event Tree

Event Tree 是本项目分析机制的统一框架。

目标：

- 把攻击、命中、伤害、攻击特效、冷却返还、增益、复活等过程拆成可追踪事件；
- 区分事实、推导、实验结论；
- 为英雄、海克斯、装备之间的交互建立统一描述。

---

# Current Event Types

- Attack
- On-Attack
- Hit
- Spell Hit
- Apply On-Hit
- Spell Damage
- Spellblade
- Buff
- Debuff
- Proc
- Damage Resolution
- Cooldown Modifier
- Cooldown Reset
- Delayed Trigger
- Revive
- Critical Check
- Projectile Split
- Proc Chain
- Cooldown Listener
- Death Check
- On Kill Effects

---

# Attack Event Tree

普通攻击推荐拆成以下事件线：

```text
Attack
↓
On-Attack
↓
Hit
↓
Apply On-Hit
↓
Spellblade
↓
Buff / Debuff
↓
Proc
↓
Damage Resolution
```

关键检查点：

| Stage | What To Check |
|---|---|
| Attack | 是否是普通攻击动作，是否被 Attack Modifier 改写 |
| On-Attack | 是否消耗/准备 Spellblade，是否触发攻击宣告监听器 |
| Hit | 是否命中，是否暴击，是否被 Hit Listener 监听 |
| Apply On-Hit | 是否执行 On-Hit Pool，执行几轮，是否产生额外 Apply |
| Spellblade | Trinity Force、Lich Bane 等是否在此处结算 |
| Buff / Debuff | 是否施加状态，状态是否继续触发后续事件 |
| Proc | Mystic Punch、Phenomenal Evil、Quest 等监听器是否触发 |
| Damage Resolution | 最终伤害、减免、护盾、死亡判定 |

额外 Apply 来源需要单独标注可信度：

- Dusk and Dawn：待验证是否再次 Apply；
- Double Tap：待验证具体触发边界；
- champion skill re-apply：按英雄逐项验证；
- other augment/item sources：按来源记录。

---

# Spell Event Tree

技能推荐拆成以下事件线：

```text
Spell Cast
↓
Spell Hit
↓
Spell Damage
↓
Apply On-Hit (if available)
↓
Buff / Debuff
↓
Proc
↓
Damage Resolution
```

关键检查点：

- 技能是否有 Spell Hit；
- 技能伤害是否属于 Spell Damage；
- 技能是否自带 Apply On-Hit，或被 Ethereal Weapon 等效果赋予 Apply On-Hit；
- 技能是否施加 Buff / Debuff；
- 是否存在 Delayed Trigger；
- 是否触发 Cooldown Listener、Quest、Phenomenal Evil、Mystic Punch 等监听器。

---

# Analysis Rule

任何机制分析先回答：

1. 触发源是什么？
2. 产生了哪些事件？
3. 哪些事件被海克斯/装备监听？
4. 监听的是 Hit、Apply On-Hit、Spell Damage，还是其他事件？
5. 结论来源是官方、实验，还是理论？

---

# Expansion Queue

后续应逐步细化以下事件：

- Critical Check：暴击判定在 Hit/伤害计算中的位置；
- Projectile Split：弹体分裂是否继承原始事件；
- Proc Chain：触发效果是否继续触发其他监听器；
- Cooldown Listener：冷却返还/重置监听哪个事件；
- Death Check：处决、复活、死亡后效果的判定顺序；
- On Kill Effects：击杀/参与击杀/尸体爆炸等后续事件。
