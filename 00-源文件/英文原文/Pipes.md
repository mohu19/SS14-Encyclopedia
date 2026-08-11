# 管道（EN 源文件）

> 条目ID: `Pipes` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Pipes
  Pipes are used to distribute gasses from one place to another.
  There are a wide variety of pipes available to construct:

  
    [[实体:GasPipeStraight]]
    [[实体:GasPipeHalf]]
    [[实体:GasPipeBend]]
    [[实体:GasPipeTJunction]]
    [[实体:GasPipeFourway]]
  

  Pipes will <span style="color:#a4885c">automatically connect</span> to other pipes when anchored (or wrenched) to the hull to form a [textlink="network of pipes." link="PipeNetworks"]
  A network of pipes is commonly called a [textlink="pipenet" link="PipeNetworks"].

  Pipes will <span style="color:red">not connect</span> to pipes that are already connected to a different pipe.
  For example, building a bent pipe on top of a straight pipe to form a makeshift T-junction will not work.

  However, two pipes can share a tile as long as one isn't obstructing the other's connection to another pipe.
  For example, two bend pipes can be placed on the same tile, with one moving gas from north to east, and the other moving gas from west to south.

  You can color pipes (and most equipment that handles gasses) using a spray painter.
  This is commonly done to distinguish the air and waste components of the station's Distro pipenet.
