# 管网（EN 源文件）

> 条目ID: `PipeNetworks` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Pipe Networks
  Pipe networks — commonly called Pipenets — are a series of interconnected [textlink="pipes" link="Pipes"], usually with a common task.

  
    [[实体:GasPipeStraight]]
    [[实体:GasPipeHalf]]
    [[实体:GasPipeBend]]
    [[实体:GasPipeTJunction]]
    [[实体:GasPipeFourway]]
    [[实体:GasPressurePump]]
    [[实体:GasVolumePump]]
  

  Pipenets are used all throughout the station to deliver, remove, or otherwise move gas throughout it.
  Great examples are the station's Distro or Wastenet, which deliver breathable air and remove waste gas, respectively.

  ## How Pipenets Work
  In Space Station 14, pipenets behave as a whole, defined volume, with input/output points at the ends of the network.
  Forcing or vacuuming gas in or out using a [textlink="pump" link="Pumps"] will affect the entire network, not just the pipe it's connected to.

  Pipenets are only separated by devices capable of interrupting flow, or by certain devices.
  For example, a [textlink="Pressure Pump" link="Pumps"] will not allow gas to flow through it unless it's powered and has gas to pump.

  Some examples of devices that separate pipe networks are:
  - [textlink="Pressure and Volumetric Pumps" link="Pumps"]
  - [textlink="Gas Mixers and Filters" link="MixingAndFiltering"]
  - [textlink="All Valves" link="Valves"]
  - [textlink="Radiators" link="Radiators"]

  An example of a pipenet being seperated into two, distinct pipenets by a [textlink="pump" link="Pumps"] is shown below:
