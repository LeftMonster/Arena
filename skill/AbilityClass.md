# Ability Class

Ability Class 是本项目在进入单个英雄研究前使用的英雄能力分类。

目的：

- 先判断英雄主要靠哪类事件链输出或提供功能；
- 再决定 Ability Augments、Quest Augments、海克斯、装备和实验的分析顺序；
- 避免把所有英雄都强行套入 On-Hit 模型。

来源：

- 旧上下文 `LoL_Mechanics_Project_Latest_v3/Skill_v9_SpellHero_Framework.md`
- 旧上下文 `LoL_Mechanics_Project_Latest_v3/Roadmap_v7_Update.md`

---

# Current Classes

| Class | Meaning | Example | Main Questions |
|---|---|---|---|
| On-Hit Carry | 主要通过普攻和攻击特效池输出 | Master Yi | Hit Count、Apply Count、攻击特效池、Mystic Punch 监听事件 |
| On-Hit Caster | 技能可执行攻击特效，技能与 On-Hit 混合 | Gangplank, Ezreal | 哪些技能是 Consumer、是否按目标独立 Apply |
| Spell Combo | 技能循环和连招顺序决定输出 | Ryze | Ability Augment 是否改变核心循环和冷却瓶颈 |
| Spell Utility | 技能提供控制、增益、减益、复活或延迟触发 | Zilean | Buff/Debuff、Delayed Trigger、Cooldown Reset、Revive |
| Spellblade Hero | 技能施放与咒刃/下一次攻击绑定 | Corki | Spellblade 是否是核心事件，是否能被海克斯放大 |
| Attack Modifier Hero | 技能修改普通攻击本身，而不是简单 On-Hit | Ashe | On-Attack、Attack Modifier、Hit 与 Apply 是否分离 |
| Summoner | 召唤物承担部分输出或触发 | 待补 | 召唤物是否继承海克斯/装备/攻击特效 |
| Trap | 陷阱或预置物触发伤害/控制 | 待补 | 触发者归属、Spell Hit、Proc、冷却返还 |

---

# Research Order

推荐顺序：

1. Ability Class
2. Ability Augments
3. Quest Augments
4. Event Tree
5. Normal Augments
6. Items
7. Experiments
8. Hero Archive

原因：

- Ability Augment 可能让同一个英雄变成另一个分析对象；
- 不同 Ability Class 监听的事件不同；
- 先分类可以减少重复实验和错误构筑推导。

---

# Spell Utility Framework

Spell Utility 英雄优先检查：

1. Ability Augments
2. Event Tree
3. Buff / Debuff
4. Cooldown Modifier
5. Cooldown Reset
6. Delayed Trigger
7. Quest Augments
8. Normal Augments
9. Items
10. Experiments

典型事件树：

```text
Cast
↓
Spell Hit
↓
Apply Buff / Debuff
↓
Delayed Trigger
↓
Spell Damage
↓
Proc
↓
Final Result
```

Zilean 示例：

- Ability Class：Spell Utility
- Q：Delayed Trigger
- W：Cooldown Reset
- E：Buff / Debuff
- R：Revive

---

# Case Notes

Master Yi：

- 默认 Class：On-Hit Carry
- 重点：Q Apply On-Hit、E True Damage、Mystic Punch、Ethereal Weapon、Dusk and Dawn

Gangplank：

- 默认 Class：On-Hit Caster
- 重点：Barrel、Spellblade、On-Hit interactions

Ryze：

- 默认 Class：Spell Combo
- 重点：如果 Ability Augment 重置 E 冷却，则 E 可能从普通技能变成循环发动机

Corki：

- 默认 Class：Spellblade Hero
- 注意：当前被动特殊支持 Spellblade，不应简单归类为泛 On-Hit

Ashe：

- 默认 Class：Attack Modifier Hero
- 重点：攻击修正、On-Attack、Hit 与 Apply 的边界

---

# Status

当前可信度：

- Class 名称和分类是项目内部分析框架；
- 具体英雄归类是研究入口，不是最终结论；
- 每个英雄最终仍需用官方文本、客户端文本和实验复核。
