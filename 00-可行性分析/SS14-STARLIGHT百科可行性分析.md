# SS14（STARLIGHT 星光服务器）百科可行性分析

> 分析对象：[sernseek/space-station-14](https://github.com/sernseek/space-station-14)（`starlight-dev` 分支）
> 源码克隆：`C:\Users\33922\projects\SS14-Starlight\`（sparse 部分克隆，104MB）
> 分析日期：2026-08-10

---

## 一、项目定位：这是什么

这是一个 **Space Station 14 的深度定制 fork**——STARLIGHT（星光）服务器。定位与 TianGuan13 之于 NovaSector 完全同构：在官方 SS14 基础上叠加大量自研"独特机制"，并额外缝合了十几个社区 fork 的定制层（Impstation、Funkystation、FarHorizons、Moffstation、CP14 中世纪文明等）。

- 默认分支：`starlight-dev`
- 语言：**C#（.NET）**，非 SS13 的 BYOND DM
- 引擎：RobustToolbox（子模块）
- 规模：源码 9120 个 C# 文件 + 4058 个 yaml 原型文件（合计实体原型 **1.6 万+**）

## 二、SS14 vs SS13：架构差异（为什么"完全不一样"）

| 维度 | SS13（TianGuan13） | SS14（STARLIGHT） |
|---|---|---|
| 语言 | BYOND DM（脚本式） | C#（编译型，.NET 8） |
| 架构 | 传统 OOP 继承树（`/obj/item/...` 多层继承） | **ECS**（Entity-Component-System） |
| 内容定义 | DM 代码内联定义（`obj/item/backpack` + var） | **yaml 原型**（`- type: entity`，纯数据） |
| 行为逻辑 | 对象方法（`proc/attack()` 覆写） | **System 类**（如 `ChangelingSystem`，按组件组合驱动） |
| 定制层 | `code/` + `modular_nova/` 双源 | 上游 `Resources/Prototypes/` + **`_Starlight/` 前缀层**（同名覆盖） |
| 继承 | DM 父类型链 | yaml `parent:` 字段 + 组件组合 |
| 数值参数 | 代码中 var 声明 | yaml 组件字段（`damageModifierSet` 等直接可读） |

**核心差异一句话**：SS13 的数据和逻辑混在 DM 代码里；SS14 把"数据"（yaml 原型）和"逻辑"（C# System）彻底分离。

### 对百科提取的影响（关键结论）

1. **物品/结构/生物/化学的定义提取 → 比 SS13 容易得多**
   - SS13 需要 grep DM 代码、追继承链、读 var 声明
   - SS14 的 yaml 原型自带 `id` / `name` / `description` / `parent` / `components` 结构化字段，一个文件可程序化批量解析（`name:` + `description:` 就是百科条目骨架，`parent:` 就是继承关系）
   - 已实测样例：背包 yaml 中 `name: roboticist backpack` / `description: A backpack specifically designed for oil...` 直接可作词条引言

2. **机制行为（怎么用、效果、时序）→ 需要读 C# System，但结构更清晰**
   - 每个机制对应一个明确的 System 类（如 `ChangelingSystem.cs` 620 行承载变形怪全部能力）
   - C# 是强类型编译语言，命名规范、注释可读性远好于 DM 的松散脚本
   - 需要建立"yaml 组件字段 → C# System 行为"的对照阅读法

3. **继承与覆写 → `_Starlight/` 层是百科真值的"覆写优先"源**
   - SS14 同 id 原型后者覆盖前者（加载顺序），`_Starlight` 层同名文件/实体覆盖上游
   - 与 NovaSector 双源铁律（`code/` + `modular_nova/`）完全同构，方法论可平移

## 三、内容盘子盘点（数据规模）

| 类别 | 数量 | 说明 |
|---|---|---|
| 实体原型总数 | **~16,700** | 上游 9270 + `_Starlight` 7079 + 其他 fork 层 ~450 |
| 原型 yaml 文件 | 4058 | |
| C# 源文件 | 9120 | Server + Shared + Client |
| 化学试剂 `reagent` | 467 | 含 `_Starlight` 自研试剂 |
| 反应配方 `reaction` | 340 | |
| 研究科技 `technology` | 96 | |
| 地图 | 有 Lavaland（拉瓦兰）等 | `Resources/Maps/_Starlight` |

**星光自研特色系统**（`Content.Server/_Starlight/` 60+ 目录）：CosmicCult 宇宙邪教、Vampires 吸血鬼、Changeling 变形怪、Devil 恶魔、Shadekin、Terminator 终结者、Xenobiology/Xenoborgs、Bluespace 蓝空间、Cybernetics 赛博义体、Surgery 手术、CryoTeleportation、Railroading、SecureTerminal、Wreckswarms 等——大量概念与 SS13 机制对应（变形怪/义体/邪教/拉瓦兰），但实现完全不同。

**内置 Guidebook**（游戏内百科，yaml 驱动）：官方 + 星光两层，已按 `medical / engineering / security / chemicals / antagonist / cargo / science` 部门组织——**这就是现成的百科目录骨架**，与 SS13 百科"按游戏内部门分类"铁律完全一致。

## 四、可行性结论：✅ 能做，且提取效率高于 SS13

**可以做**，甚至比 SS13 百科更系统化，理由：

1. **数据层提取自动化程度高**：yaml 是结构化数据，可用脚本批量解析出"实体清单 + 名称 + 描述 + 继承链 + 组件参数"，天然生成词条骨架和全量清单（对应你"有多少写多少、禁只列精选"的硬要求）
2. **目录骨架现成**：官方 + `_Starlight` 双层 Guidebook 已按部门分好类
3. **定制层模式熟悉**：`_Starlight` = TianGuan13 的 `modular_nova`，方法论直接平移
4. **语言可读性**：C# System 比 DM 更规范，机制细节提取（数值、阈值、配方产物）更可靠

### 需要调整的方法论（相对 SS13）

| SS13 方法 | SS14 替代 |
|---|---|
| grep `.dm` 定义 | 解析 `Resources/Prototypes/**/*.yml`（`^- type: entity`） |
| 追 DM 继承链 | 看 yaml `parent:` 链 + 组件组合 |
| 读 proc 逻辑 | 读 `Content.*/_Starlight/<System>/<System>System.cs` |
| NovaSector 双源铁律 | `_Starlight` 层覆写优先（同 id 后加载覆盖） |
| 部门分类铁律 | 沿用 + 参考 Guidebook 目录 |

## 五、风险与挑战

1. **体量巨大**：1.6 万实体 + 多 fork 缝合。需要先定优先级（建议：`_Starlight` 自研内容 > 上游差异内容 > 其他 fork 层），避免一开始就铺全量
2. **多 fork 层归属**：`_CP14`（中世纪）等层内容是否实际启用需验证（看 game_presets / secret_weights / 地图引用），分类时需按"玩家实际能玩到"过滤
3. **无中文 locale**：`Resources/Locale/` 只有 en-US / nl-NL，所有词条名需要自行翻译（这正好是百科的工作量核心）
4. **版本漂移**：fork 更新频繁，百科需记录分析基线 commit
5. **引擎层**：RobustToolbox 未拉取（sparse 排除），纯机制分析一般不需要，但涉及引擎级行为（物理/渲染）时需补拉

## 六、建议执行路径（若确认开工）

1. **Phase 0 — 基线盘点**：脚本解析全部 yaml → 生成实体全清单（id/名称/描述/父类/所属层），按部门归类，产出"百科遗漏清单"式的主索引
2. **Phase 1 — 部门卷**：沿用 SS13 百科部门结构（01-医疗部 / 02-安保部 / 03-工程部 / 04-供应部 / 05-服务部 / 06-科学部 / 07-角色与种族 / 08-事件与管理 / 09-反派 等），先写 `_Starlight` 自研 + 有差异的内容
3. **Phase 2 — 机制深挖**：每个自研 System（CosmicCult / Vampires / Changeling / Terminator / Railroading / SecureTerminal...）逐篇独立成章，数值全部回源码验证
4. **Phase 3 — 覆盖核验**：全仓库搜索验证（yaml + cs 双源），对齐"文档宣称数量 = 实际定义数量"

> 本报告结论基于 `starlight-dev` 分支 commit 2026-07-29 的 sparse 部分克隆（Prototypes + Content.* + Locale）。
