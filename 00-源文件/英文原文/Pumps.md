# 泵（EN 源文件）

> 条目ID: `Pumps` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
# Pumps
  Pumps are the primary way of actively moving gasses through a [textlink="pipenet." link="PipeNetworks"]
  They take gas from one side and push it to the other.
  There are two different types of pumps:

  
    [[实体:GasPressurePump]]
    [[实体:GasVolumePump]]
  

  Some important things to note about pumps:
  - Pumps <span style="color:#a4885c">require power</span> through a nearby LV cable to function.
  - Pumps output on the side with the red stripe.
  - Gas cannot move backwards through pumps (although if you are using a pump to do solely this, you should use the [textlink="passive gate" link="PassiveGate"] instead).
  - Pumps cannot move gasses into pipes with pressures or volumes exceeding their <span style="color:#a4885c">limit</span>. This causes them to be <span style="color:red">blocked</span>.

  Pumps will show a colorful animation when they are doing work.
  If they have no gas to pump or they are blocked, they will show a blinking <span style="color:red">red</span> animation.
  Pumps that are off, have no power, or are unanchored will show no animation.

  ## Pressure Pumps
  Pressure pumps are the most common type of pump.
  They move gas based on <span style="color:#a4885c">pressure</span>, making them useful for controlling the exact pressure of a pipe, or for drawing a vacuum.

  
    [[实体:GasPressurePump]]
  

  A pressure pump <span style="color:red">cannot</span> move gas to a pipe that has a pressure higher or equal to the pressure set on the pump.

  For example, a pressure pump cannot pump gas to a pipe that is currently at 500 kPa, if the pressure pump is set at 500 kPa.

  Pressure pumps can pump up to a maximum pressure of <span style="color:orange">[protodata="GasPressurePump" comp="GasPressurePump" member="MaxTargetPressure"/] kPa</span>.
  They will become <span style="color:red">blocked</span> if they try to push gas into a pipe higher than this pressure.

  ## Volumetric Pumps
  Volumetric pumps are an alternative pump, moving gas based on <span style="color:#a4885c">volume</span>.

  
    [[实体:GasVolumePump]]
  

  They are extremely useful for moving large amounts of gas quickly.
  They can typically achieve higher pressures than a pressure pump.

  While volumetric pumps work off of the principle of volume, they will become <span style="color:red">blocked</span> if they try to push gas into a pipe higher than <span style="color:orange">[protodata="GasVolumePump" comp="GasVolumePump" member="HigherThreshold"/] kPa</span>.
