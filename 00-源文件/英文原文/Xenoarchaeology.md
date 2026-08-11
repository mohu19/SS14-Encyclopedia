# 异星考古学（EN 源文件）

> 条目ID: `Xenoarchaeology` ｜ 来源层: official ｜ 分类: science
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Xenoarchaeology

  Xenoarchaeology is a branch of Science focused on researching alien **artifacts**.

  Unlocking their secrets grants research points and reveals strange, potentially useful, or dangerous effects.

  At round start, Science usually has one or two artifacts in the lab. More can be:
  - Ordered from <span style="color:orange">Cargo</span>
  - Found by <span style="color:orange">Salvage</span>
  - Assembled from **fragments**
  - Appear during certain station events

  ## Artifacts
  
    [[实体:ComplexXenoArtifact]]
    [[实体:ComplexXenoArtifactItem]]
  

  Artifacts contain **nodes** arranged in **layers**.
  - Unlocking a node unlocks connected nodes on upper layers.
  - Each node has **triggers**, actions that must be performed near the artifact to unlock a node.
  - When a node is unlocked, its **effect** will trigger, and the node becomes **<span style="color:plum">Active</span>**.
  - Each node has **durability**: the number of times it can be manually activated after being unlocked.
  - Higher nodes are harder to reach but give more **research points**.
  - Unlocking all nodes provides no special bonus, but every node yields research points.

  ## Equipment
  
    [[实体:MachineArtifactAnalyzer]]
    [[实体:ComputerAnalysisConsole]]
    [[实体:NodeScanner]]
  
  - **Artifact Analyzer:** Stationary device that scans artifacts, sending data to the Console.
  - **[textlink="Analysis Console:" link="AnalysisConsole"]** Stationary device that is used to display the node tree. Must be linked to an Analyzer with a multitool.
  - **Node Scanner:** Small hand-held device that can show the ID of the node currently being activated and whether the artifact is ready to trigger, letting scientist have minimal required knowledge for operating inside chamber near artifact and far without direct access to console.

  
    [[实体:CrateArtifactContainer]]
    [[实体:HandheldArtifactContainer]]
  
  - **Artifact Containers:** Safely store and transports artifacts and prevent nodes from triggering.
  
    [[实体:MachineArtifactCrusher]]
  
  - **Artifact Crusher:** Crushes artifacts into fragments. Four fragments can be rebuilt into a new artifact.
  
    [[实体:ArtifactFragment]]
  
  - **Artifact Fragment:** Pieces of destroyed artifacts. Four fragments can be rebuilt into a new artifact using the craft menu.
