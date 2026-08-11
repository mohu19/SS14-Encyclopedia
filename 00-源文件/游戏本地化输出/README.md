# 游戏本地化输出（Guidebook 中文正文）

> 由 `tools/convert_localization.py` 生成：**英文 Guidebook XML 结构骨架 + 中文译文文本回填**。
> 产出为游戏可直接使用的 XML（放入仓库 `Resources/ServerInfo/zh-CN/Guidebook/` 对应路径即可在游戏内显示中文 Guidebook）。

## 说明

- **覆盖**：官方层 329 个 Guidebook 正文条目（zh-cn 分支缺中文正文的部分）
- **结构**：`<Document>/<Box>/<GuideEntityEmbed>/[color]/[bold]/[italic]/[textlink]` 全部保留（从英文源恢复，embed 实体 ID 不丢）
- **标题**：一级标题 = 中文条目名（对应 zh-CN ftl 的 guide-entry-* 显示名，已有 370 个映射）
- **术语**：已按官方 zh-CN 译名统一（变形怪→拟形怪、熵化巨像→熵灭巨像、零空间→虚无空间等）
- **星光层**（`_Starlight/Guidebook/`）：zh-cn 分支已有中文，无需转换（未包含）

## 使用

1. 把 `ServerInfo/zh-CN/` 内容并入星光服务器仓库对应目录
2. 游戏内 Guidebook 即显示中文（配合已有 zh-CN locale + guide-entry 显示名）

## 已知边界

- 英文源 Box 标记破损的文件（如 SLCrimeList 16/176）忠实保留源结构
- 译文段落拆分处文本并入前段（内容不丢，段落边界可能合并）
