# 被动单向阀（EN 源文件）

> 条目ID: `PassiveGate` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Passive Gate
  The passive gate is a simple one-way valve that prevents gasses from flowing backwards.
  
    [[实体:GasPassiveGate]]
  

  The valve's input is on the side of the <span style="color:red">red</span> circle.
  The valve also shows the current flow rate of the pipe when examined.

  It's useful in many applications, for example:
  - Preventing a pure gas from getting contaminated via a mixed gas flowing back through the pipe.
  - Preventing pressure or temperature changes across two [textlink="pipenets" link="PipeNetworks"] in the opposite direction.
  - Quickly checking the flow rate on a pipenet without needing a [textlink="gas analyzer" link="AtmosTools"].
