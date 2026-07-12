# Ryze

## Hero

Ryze / 瑞兹

## Ability Class

Spell Combo

瑞兹的核心不是普攻事件线，而是技能循环：

```text
Spell Cast
↓
Spell Hit
↓
Spell Damage
↓
Cooldown Listener / Reset
↓
Next Spell Cast
```

## Ability Augments

### 超负荷 / Overloaded

当前效果：

- 使用另一个技能会重置【所选技能】技能的冷却时间。

当前判断：

- 如果【所选技能】映射到瑞兹 E，则它应作为瑞兹首选 Ability Augment；
- 该效果会把 E 从普通技能变成循环发动机；
- 分析优先级高于普通 AP、技能急速、技能命中类海克斯。

事件树变化：

```text
E
↓
Q / W / R / other spell
↓
Reset E cooldown
↓
E
↓
Next spell
↓
Reset E cooldown
```

需要复核：

- 当前正式服是否一定把 Overloaded 映射到瑞兹 E；
- R 是否参与触发“另一个技能”；
- 重置是否受技能命中、施放成功、目标存在等条件限制；
- 与大法师、尤里卡、炼狱导管等冷却类海克斯是否存在递增或浪费。

## Quest Augments

待补。

## 技能事件（Skill Events）

- Q：主要 Spell Damage / Spell Hit 来源，受 E 标记影响。
- W：控制/减速类 Spell Utility 事件，可能参与 E 重置链。
- E：核心循环技能；若被 Overloaded 强化，则变成循环发动机。
- R：战略位移/传送技能；是否触发 Overloaded 需要实测。
- Passive：法力和 AP 相关成长，需要与法力型海克斯一起分析。

## Event Tree

基础瑞兹：

```text
E
↓
Q
↓
W / E / Q
↓
Spell Damage
↓
Proc
```

Overloaded E 瑞兹：

```text
E
↓
Any other ability
↓
Reset E cooldown
↓
E
↓
Repeat
```

## 推荐海克斯

首选：

1. 超负荷 / Overloaded

后续优先：

1. 大法师 / Archmage
2. 超凡邪恶 / Phenomenal Evil
3. 尤里卡 / Eureka
4. 炼狱导管 / Infernal Conduit
5. 魔法飞弹 / Magic Missile
6. 无限循环往复 / Infinite Recursion
7. 由心及物 / Mind to Matter

说明：

- 如果 Overloaded 可选并映射到 E，先拿 Overloaded；
- 普通 AP/技能急速类海克斯是第二层；
- 普攻/On-Hit 类不是主线。

## 推荐装备

待补。

## Experiments

EXP-RYZE-001：

验证 Overloaded 是否在瑞兹上强化 E。

EXP-RYZE-002：

验证 Q/W/R 是否都能触发 Overloaded 的 E 冷却重置。

EXP-RYZE-003：

验证 Overloaded + Archmage / Eureka / Infernal Conduit 是否出现冷却收益溢出或循环质变。

## Evidence

- `augments/AramMayhem_AlignedData.csv`：Overloaded / 超负荷，效果为“使用另一个技能会重置【所选技能】技能的冷却时间。”
- `skill/AbilityClass.md`：瑞兹归类为 Spell Combo；旧上下文已记录“如果 Ability Augment 重置 E 冷却，则 E 可能从普通技能变成循环发动机”。

## Patch History

待补。

## Open Questions

- Overloaded 的瑞兹技能映射是否为 E？
- R 是否触发 E 重置？
- E 重置循环是否改变瑞兹海克斯优先级到“冷却监听/技能施放”路线？
