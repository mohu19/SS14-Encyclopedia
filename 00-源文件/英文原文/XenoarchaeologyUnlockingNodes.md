# 解锁节点（EN 源文件）

> 条目ID: `XenoarchaeologyUnlockingNodes` ｜ 来源层: official ｜ 分类: science
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Unlocking Nodes
  
    [[实体:ComplexXenoArtifact]]
    [[实体:ComplexXenoArtifactItem]]
  

  To activate and unlock nodes on an artifact, you should:
  - Check a node on the **Analysis Console** to check its triggers and effects.
  - Perform the **triggers** listed in the console. Some require direct interaction with the artifact, while others may only need the correct environment or a specific action performed nearby.
  - Once a trigger is successfully performed, the artifact will respond with the message: *"It begins to shift in strange ways..."*. The **Node Scanner** will then indicate which specific nodes are being triggered.

  Artifacts enter an unlocking state after the first trigger is met. During this state, any remaining triggers must be completed. The unlocking window initially lasts a few seconds and resets each time a new trigger is activated. This window grows longer with each additional node unlocked, giving more time to complete further triggers.

  Once all required triggers are completed successfully, the artifact will trigger it's effect and a popup will appear saying: *"It slows down, visibly changed."*, and the node will appear as **<span style="color:plum">Active</span>** on the Console.

  If an artifact fails to activate, it will stop resonating and display the message: *"It slows down before uneventfully stopping."* After this, it enters a cooldown period before it can be activated again.

  The order of trigger activation **does not matter** for individual nodes. *However*, some triggers affect multiple nodes. As a rule of thumb, start with a trigger that is unique to the node you want to unlock. Activating a trigger for a different node during this phase prevents the target node from unlocking until the artifact’s cooldown ends.

  

  ## Active Nodes
  Once unlocked, a node is considered active. Only the highest unlocked nodes in a tree’s layer are activatable, lower nodes in the same tree cannot be triggered anymore once a higher node has been activated.

  Artifacts often have multiple trees. Layer precedence applies within each tree, but different trees operate independently. This means nodes in different trees can be activated simultaneously as long as they are the highest unlocked nodes in their respective trees.

  **Manual activation triggers all unlocked nodes at once and consumes durability.**

  

  ## Triggers
  Examples include:
  - Examining the artifact
  - Playing an instrument
  - Damaging or throwing it
  - Exposing it to gases (plasma, tritium, etc.)
  - Changing pressure or temperature
  - Using tools (screwdriver, multitool, crowbar, wrench)
  - Splashing reagents (blood, water, ammonia, etc.)
  - Killing something nearby

  ## Effects
  Effects can be:
  - <span style="color:green">Harmless:</span> producing plants, animals, or junk
  - <span style="color:#00ccff">Helpful:</span> charging batteries, creating instruments or money
  - <span style="color:red">Hazardous:</span> anomalies, radiation, explosions, hostile fauna
