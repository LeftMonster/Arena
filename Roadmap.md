# Roadmap

当前项目目标：建立可追溯、可查询、可实验复现的 LoL ARAM: Mayhem / Arena-style Augments 机制数据库。

---

# Phase 1: Official Source Baseline

状态：进行中。

目标：

- 整理 Riot 官网补丁说明和开发者文章；
- 建立官方源索引；
- 区分当前确认池、已移除池、历史待复核池。

当前文件：

- `augments/OfficialSourceIndex.md`
- `augments/Database.md`

---

# Phase 2: Client Tooltip Database

状态：下一步。

目标：

- 补当前正式服完整 tooltip；
- 补国服官方中文名；
- 补 tier、augment type、current status；
- 把官网只有名称的条目补成可查询记录。

采集路径：

- 优先使用 CDragon / 客户端静态数据；
- 静态数据不足时，使用正式服客户端截图或真机浏览器采集；
- 如遇网页反爬、JS 渲染、登录态或地区化限制，可使用用户提供的去爬虫特征自动化浏览器；
- 详细策略见 `DataAcquisition_Plan.md`。

---

# Phase 3: Ability Class And Ability Augments

状态：待开始。

研究顺序：

Ability Class → Ability Augments → Quest Augments → Event Tree → Normal Augments → Items → Experiments → Hero Archive

原因：

不同 Ability Class 的英雄应采用不同分析框架，不能统一套用 On-Hit 模型。

---

# Phase 4: Mechanism Models

状态：进行中。

当前模型：

- `skill/ApplyCount.md`
- `skill/EventTree.md`

后续模型：

- Hit vs Apply
- Spellblade
- Cooldown Reset
- Buff / Debuff
- Revive

---

# Phase 5: Hero Archive

状态：待开始。

优先英雄：

- Master Yi
- Gangplank
- Ryze
- Corki
- Zilean
- Ashe

模板：

- `heroes/_HeroTemplate.md`
