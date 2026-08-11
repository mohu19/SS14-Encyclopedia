# 游戏本地化输出（Guidebook 中文正文）

> 由 `tools/convert_localization.py` 生成：**英文 Guidebook XML 结构骨架 + 中文译文文本回填**。
> 产出为游戏可直接使用的 XML——迁入星光服务器仓库后，游戏内 Guidebook 即显示中文。

## 📋 迁入指南（把中文 Guidebook 装进星光服务器）

### 1. 前提确认

| 检查项 | 说明 |
|---|---|
| 目标仓库 | `sernseek/space-station-14`（STARLIGHT fork），**zh-cn 分支** |
| 显示名 | 已就绪：zh-CN ftl 有 370 个 `guide-entry-*` 映射（条目名自动显示中文） |
| 星光层 | `_Starlight/Guidebook/` 在 zh-cn 分支**已有中文**，无需动 |
| 本包内容 | 仅**官方层缺失的中文正文**（328 个 XML） |

### 2. 迁入步骤

```bash
# 1) 进入星光仓库（zh-cn 分支）
cd <星光仓库>
git checkout zh-cn

# 2) 复制中文正文到 ServerInfo（覆盖/新增，路径镜像英文）
cp -r "<百科>/00-源文件/游戏本地化输出/ServerInfo/zh-CN/" Resources/ServerInfo/
# 结果：Resources/ServerInfo/zh-CN/Guidebook/**/*.xml（官方层中文正文）

# 3) 提交
git add Resources/ServerInfo/zh-CN/
git commit -m "localization: official Guidebook content in Chinese (328 entries)"
git push
```

### 3. 游戏内验证

1. 启动服务器，游戏内打开 Guidebook（`F1` 或对应快捷键）
2. 抽查：工程部 → 超物质引擎 / 医疗部 → 药品 / 反派 → 叛徒 等条目
3. 预期：**条目名中文 + 正文中文 + 实体嵌入图片/色标/链接正常**
4. 若某条目仍显示英文 → 检查该 XML 是否在 `ServerInfo/zh-CN/Guidebook/` 对应路径

### 4. 已知边界（迁入时留意）

| 项 | 说明 |
|---|---|
| Box 标签 | 英文源本身破损的文件（如 SLCrimeList 16/176）忠实保留源结构，不影响渲染 |
| 段落合并 | 译文段落拆分处并入前段（内容不丢，边界可能合并） |
| 化学/专名 | 化学品名（Bicaridine 等）按规范保留英文，条目内中文占比天然低 |
| 术语 | 已按官方 zh-CN 统一（拟形怪/熵灭巨像/虚无空间），与游戏内 locale 一致 |

### 5. 重新生成（百科更新后同步本地化）

```bash
cd C:\Users\33922\projects\SS14-Starlight
python tools/convert_localization.py   # 重新生成 328 个 XML
# 产物在 <百科>/00-源文件/游戏本地化输出/ServerInfo/zh-CN/Guidebook/
# 再按第 2 步复制到星光仓库
```

### 6. 文件清单（328 个）

- `Guidebook/Antagonist/`（21 个）— 反派条目
- `Guidebook/Cargo/`（3）· `Guidebook/Chemicals*`（10）· `Guidebook/Command.xml` · `Guidebook/Engineering/`（59+）
- `Guidebook/Medical/`（8）· `Guidebook/Mobs/`（10）· `Guidebook/NewPlayer/`（5）· `Guidebook/ReferenceTables/`（20）
- `Guidebook/Science/`（9）· `Guidebook/Security/`（7）· `Guidebook/ServerRules/`（规则全系）
- `Guidebook/Service/`（22）· `Guidebook/SpaceStation14.xml` · `Guidebook/StarlightSOP/`（104）
- `Guidebook/Glossary.xml` · `Guidebook/Jobs.xml` · `Guidebook/Survival.xml` · `Guidebook/Writing.xml`

## 🔧 技术说明

- **结构**：`<Document>/<Box>/<GuideEntityEmbed>/[color]/[bold]/[italic]/[textlink]` 全部保留（从英文源恢复，embed 实体 ID 不丢）
- **标题**：一级标题 = 中文条目名（对应 `guide-entry-*` ftl key）
- **标记**：color/bold/italic 配对差值 0；textlink link 全篇顺序回填；无 markdown 残留
- **数据基线**：`7f25e682`（zh-cn 分支 2026-07-26）
