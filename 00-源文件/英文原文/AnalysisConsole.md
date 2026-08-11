# 分析控制台（EN 源文件）

> 条目ID: `AnalysisConsole` ｜ 来源层: official ｜ 分类: science
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Analysis Console

  The Analysis Console is a device used to interface with artifacts. It can be used to check nodes, their triggers and effects, and extract points.

  
    [[实体:ComputerAnalysisConsole]]
  

  The console displays detailed information about each node in the artifact’s tree structure. This includes:
  - **ID:** Unique identifier for use with the Node Scanner.
  - **Class:** The layer name, nodes on the same layer share it.
  - **Status:**
  - *<span style="color:red">Locked</span>* by default.
  - *<span style="color:plum">Active</span>* when first triggered.
  - *<span style="color:lime">Unlocked</span>* if a deeper node is reached (prevents manual activations).
  - **Durability:** Number of manual activations available.
  - **Effect:** What happens when the node activates or is manually triggered.
  - **Triggers:** Required actions to unlock the node.
  - **Server:** Choose the research server where extracted points are sent.
  - **Extract Points:** Extracts points from nodes unlocked since the last extraction.
