# Glossary v4 ------ Arena 海克斯名称规范（中英对照）

> 更新目的： 统一项目中 Arena 海克斯的命名方式。
>
> **原则：** - 优先使用游戏官方中文名称。 -
> 首次出现时，同时保留英文原名。 - 后续正文统一使用官方中文。

------------------------------------------------------------------------

# 命名规范

格式：

官方中文（English Name）

例如：

-   由心及物（Mind to Matter）
-   大法师（Archmage）
-   返璞归真（Back to Basics）
-   虚幻武器（Ethereal Weapon）
-   秘术冲拳（Mystic Punch）

------------------------------------------------------------------------

# 当前已确认

  官方中文   英文
  ---------- -----------------
  由心及物   Mind to Matter
  大法师     Archmage
  返璞归真   Back to Basics
  虚幻武器   Ethereal Weapon
  秘术冲拳   Mystic Punch

------------------------------------------------------------------------

# 检索规范

以后所有资料查询：

1.  优先使用英文名称检索（官方、Wiki、数据站）。
2.  输出知识库时使用官方中文。
3.  首次出现时保留中英双语，便于交叉验证。

示例：

正确：

由心及物（Mind to Matter）

不推荐：

心智化形（直译）

------------------------------------------------------------------------

# 备注

历史文档中若出现直译名称（例如"心智化形"），以后统一视为
**由心及物（Mind to Matter）**，后续版本逐步替换，不再新增直译名称。

---

# 机制术语

本节来自旧上下文 `Glossary_v5_Mechanics_Glossary.md` 和 `Glossary_v2_EventTerminology.md` 的迁移整理。

| Term | 项目统一理解 |
|---|---|
| Attack | 一次普通攻击动作。 |
| Hit | 一次攻击或技能成功命中目标的事件。 |
| Spell Hit | 技能成功命中目标的事件。 |
| On-Hit | 攻击特效本身，是效果，不是事件。 |
| Apply On-Hit | 执行一轮攻击特效池，是事件/动作。 |
| On-Hit Effects Pool | 当前拥有的所有攻击特效集合。 |
| On-Attack | 攻击宣告时发生的事件，早于命中。 |
| Apply On-Attack | 执行一次攻击前事件关联效果。 |
| Spell Damage | 技能自身造成的伤害，不包含后续 On-Hit、Buff、Proc。 |
| Spellblade | 施放技能后下一次普攻获得额外伤害的独立机制。 |
| Proc | 因其他事件而触发的新效果。 |
| Buff | 持续性正面状态。 |
| Debuff | 持续性负面状态。 |
| Attack Modifier | 修改普通攻击本身的机制，不等同于 On-Hit。 |
| Apply Count | 一次动作最终执行 Apply On-Hit 的总次数。 |

推荐事件顺序：

```text
Cast / Attack
↓
On-Attack
↓
Hit / Spell Hit
↓
Spell Damage
↓
Apply On-Hit
↓
On-Hit Effects Pool
↓
Spellblade / Proc
↓
Buff / Debuff
↓
Final Damage / Final Result
```

核心规则：

- On-Hit = 攻击特效；
- Apply On-Hit = 执行攻击特效；
- Hit = 命中；
- On-Attack = 攻击宣告/攻击前事件；
- Spellblade = 咒刃，独立机制；
- 文档首次出现机制术语时，优先写中文说明并保留英文原词。
