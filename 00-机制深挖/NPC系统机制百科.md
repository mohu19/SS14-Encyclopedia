# NPC 系统机制百科

> 机制深挖 · SS14 星光服务器（STARLIGHT fork）· 科学部
> 源码基线：`7f25e682`（zh-cn 分支，2026-07-26）
> 核心源码：官方 HTN `Content.Server/NPC/`（159 cs）+ `Content.Shared/NPC/`（26 cs）；星光层 `Content.Server/_Starlight/NPC/`（13 cs）+ `Resources/Prototypes/_Starlight/NPCs/`（6 文件，注意是 `NPCs` 带 s，星光无共享 NPC 层）
> 数据来源：子代理源码提取（父代理落盘整理）

---

## 1. 架构全景

官方 HTN（Hierarchical Task Network）系统 185 cs + 星光自研层 13 cs。

**原型数**：
- htnCompound **68** = 官方 55（12 文件）+ 星光 13（含 `Combat/melee.yml`、`Enemies/Abyss.yml` 内联）
- utilityQuery **13** = 官方 12 + 星光 1（`PD.yml` NearbyPDTargets）
- npcFaction **27** = 官方 16 + 星光 11（`_Starlight/ai_factions.yml`，含增量全复制式覆写）

## 2. 黑板书默认值（`NPCBlackboard.cs:19-37`）

| 键 | 默认值 |
|---|---|
| IdleRange | 7 |
| RangedRange | 10 |
| MeleeRange | 1 |
| VisionRadius / AggroVisionRadius | 10 / 10 |
| 最小-最大空闲 | 2-7s |
| MeleeMissChance | 0.3 |
| RotateSpeed | float.MaxValue |
| FollowRange / BufferRange | 7 / 10 |

**关键配置**（`CCVars.NPC.cs:7-15`）：`npc.max_updates` 默认 **128**（每 tick 活跃 NPC 更新上限）、`npc.enabled` true、`npc.pathfinding` true。

## 3. HTN 机制（`HTNSystem.cs` + `HTNComponent.cs`）

- 规划队列 `JobQueue _planQueue = new(0.004)`（:26）、单任务 CPU 时间 0.02（:489）
- 计划冷却 `PlanCooldown = 0.45f`（HTNComponent.cs:33）、`ConstantlyReplan = true`（:42）→ 每 0.45s 重规划
- 已分发旧计划"更好（BTR 字典序）才替换"（HTNSystem.cs:221-246）
- 算分 = 各 consideration 分数过曲线后**连乘的几何平均**（`NPCUtilitySystem.cs:402-416`，可只降不升）；Query limit 默认 128

## 4. 移动/转向/战斗

- 上下文转向 **12 方向**（`SharedNPCSteeringSystem.cs:5-15`）；失败寻路 3 次即停（`NPCSteeringComponent.cs:118`）；重寻路阈值 RepathRange 1.5（:116）
- NPC 触发攻击**掠飞速度 20**（`NPCCombatSystem.Ranged.cs:25`）+ 精度阈值 30°（`NPCRangedCombatComponent.cs:29`）
- **星光内联**：远程点防御电池目标不寻路直接开火（Ranged.cs:150-152）、枪机自动闭锁（:108-112）、重力加速度/摩擦拆分（SteeringSystem.cs:352-361, 512-527）、近战不刹车（melee.yml:120）

## 5. 星光自研层（13 cs 明细）

- **NPCPointDefenseSystem**（23 行，GunShotEvent → `QueueDel(target)` 直接删目标，:13-22）+ NPCPointDefenseComponent（TargetKey="Target"）
- **NpcCommand**（sethtn/setenabled 管理命令，AdminFlags.Fun）
- 3 算子：**MoveFromOperator**（283 行逃跑：12 角度逐角寻路+随机路径兜底，安全距离默认 5×1.5，:35-36）、**JumpOperator**（跳跃）、**PickAccessibleOperatorWith**（蜘蛛网寻点默认范围 7）
- **NotHungryPrecondition**（HungryPrecondition 反转副本）
- **PDTargetIFFCon**（同网格弹不回击，`NPCUtilitySystem.cs:389-396` 消费）

## 6. 战斗联动

- `NPCRetaliationSystem.cs` 星光内联 `AfterRetaliationEvent`（:58-59, 83）
- `NPCUseActionOnTargetSystem`（触手攻击，`asteroid.yml` + `Enemies/Abyss.yml` 消费者）
- 印记跟随 `NPCImprintingOnSpawnBehaviourSystem`（搜索半径 3，:21，黑板写 FollowTarget，默认 Follow=true）

## 7. NPC 实体统计

官方 `Entities/Mobs/NPCs/` 28 文件 263 实体；星光 17 文件 93 实体（合计 356 定义）；73 处 `- type: HTN` 根任务。旧野怪表 `entity_tables.yml` MaintsMonstersBasic 由 `_Starlight/GameRules/variation.yml:7` 引用（35/70 人门槛分组，权重 0.3）。

## 8. 疑点清单 ⚠️

1. 守卫机器人（scurret）`ScupperComplexCompound` 未找到定义文件（可能在未 sparse 拉取的目录）
2. 商贩 NPC 相关原型零命中——星光无独立商贩实体（可能靠玩家角色担当）
3. 任务书 `Content.Shared/_Starlight/NPC/` 路径不存在（实际零共享层）
4. `PickWithWeb` 文件名与类名不一致；官方 `DoNotEscapeCompound` 在 melee.yml 中定义但无引用（死代码）
5. `NeverCollide` 等个别算子在 `// Starlight` 注释块内的行为未比对上游
6. 最近版本 BlackboardDefaults 中 `FollowCloseRange` 等键的数值需对照上游确认

## 9. 源码引用

`NPCBlackboard.cs:19-37`、`CCVars.NPC.cs:7-15`、`HTNSystem.cs:26/221-246/489`、`HTNComponent.cs:33/42`、`NPCUtilitySystem.cs:389-416`、`SharedNPCSteeringSystem.cs:5-15`、`NPCSteeringComponent.cs:116/118`、`NPCCombatSystem.Ranged.cs:25`、`NPCRangedCombatComponent.cs:29`、`_Starlight/NPC/Systems/NPCPointDefenseSystem.cs:13-22`、`_Starlight/NPC/Operators/MoveFromOperator.cs:35-36`、`SteeringSystem.cs:352-361/512-527`、`_Starlight/NPCs/`、`ai_factions.yml`、`variation.yml:7`
