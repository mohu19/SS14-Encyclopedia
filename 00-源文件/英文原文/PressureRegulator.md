# 压力调节阀（EN 源文件）

> 条目ID: `PressureRegulator` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Inlet Pressure Regulator
  The Inlet Pressure Regulator is a passive device that allows gas to escape from a [textlink="pipenet" link="PipeNetworks"] when the pressure exceeds a certain threshold.

  
    [[实体:GasPressureRegulator]]
  

  ## Operation
  The valve will automatically <span style="color:green">open</span> when the pressure in the pipe exceeds the set threshold, allowing gas to escape to the connected output pipe.

  The valve will <span style="color:red">close</span> again when the pressure drops below the set threshold.

  The flow rate of the valve is limited to <span style="color:orange">[protodata="GasPressureRegulator" comp="GasPressureRegulator" member="MaxTransferRate"/] L/s</span>.

  ## Example Uses
  The valve is commonly used to prevent overpressure situations in gas systems, such as [textlink="TEG" link="TEG"] cooling loops and [textlink="pipes" link="Pipes"], which would cause a failure in the system (clogged [textlink="pumps" link="Pumps"]).

  The valve can also be used to vent off ready-to-use, hot gas from a burn chamber.
  For example, it may be undesirable to allow a burn chamber to drop below a specific pressure for a long time, as this may cause the gas to cool down too much and thin out, which would cause a flameout.

  An inlet pressure regulator can be used to vent off excess gas, while keeping the pressure in the burn chamber above a certain threshold, which may help in sustaining a fire in the chamber.
