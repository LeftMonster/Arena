# Event Tree

Event Tree 是本项目分析机制的统一框架。

目标：

- 把攻击、命中、伤害、攻击特效、冷却返还、增益、复活等过程拆成可追踪事件；
- 区分事实、推导、实验结论；
- 为英雄、海克斯、装备之间的交互建立统一描述。

---

# Current Event Types

- Attack
- Hit
- Apply On-Hit
- Spell Damage
- Spellblade
- Buff
- Debuff
- Cooldown Modifier
- Cooldown Reset
- Delayed Trigger
- Revive

---

# Analysis Rule

任何机制分析先回答：

1. 触发源是什么？
2. 产生了哪些事件？
3. 哪些事件被海克斯/装备监听？
4. 监听的是 Hit、Apply On-Hit、Spell Damage，还是其他事件？
5. 结论来源是官方、实验，还是理论？
