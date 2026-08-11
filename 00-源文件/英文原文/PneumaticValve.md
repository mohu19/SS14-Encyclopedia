# 气动阀（EN 源文件）

> 条目ID: `PneumaticValve` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Pneumatic Valve
  The pneumatic valve is a bidirectional valve controlled via a pressure input.
  
    [[实体:PressureControlledValve]]
  

  The pneumatic valve has 3 connections: input, output, and control.
  The "input" side will be the input/output connection with the highest pressure, and can switch sides, making the valve bidirectional.

  
    [[实体:GasPipeStraight]]
  
  
    
    [[实体:PressureControlledValve]]
    [[实体:FloorTileItemSteel]]
  
  
    [[实体:GasPipeStraight]]
  

  The valve will <span style="color:green">open</span> when the pressure on the output side is lower than the pressure on the control side by <span style="color:orange">[protodata="PressureControlledValve" comp="PressureControlledValve" member="Threshold"/] kPa</span>.

  The valve will <span style="color:red">close</span> when the pressure of the output side reaches the pressure of the control side within <span style="color:orange">[protodata="PressureControlledValve" comp="PressureControlledValve" member="Threshold"/] kPa</span>.

  For example, a pneumatic valve with a control pressure of 500 kPa will open when the output pressure is 500 kPa - <span style="color:orange">[protodata="PressureControlledValve" comp="PressureControlledValve" member="Threshold"/] kPa</span> or lower, and it will close when the output pressure is 500 kPa - <span style="color:orange">[protodata="PressureControlledValve" comp="PressureControlledValve" member="Threshold"/] kPa</span> or higher.

  The valve's control pressure is determined by a pipenet connection, and as such can be adjusted on the fly by a [textlink="pump" link="Pumps"] or another source of pressure control.

  ## Differences to Pumps

  The pneumatic valve is different from a [textlink="pump" link="Pumps"] which moves gas via work.
  The pneumatic valve is a passive device that moves gas based on the higher pressure of the input gas, and as such it can sometimes fill volumes faster than a [textlink="pump" link="Pumps"] can.

  For example, a pneumatic valve with a control pressure of 500 kPa will fill a volume faster than a pressure [textlink="pump" link="Pumps"] set to 500 kPa.
  However, the [textlink="pump" link="Pumps"] will be able to maintain the pressure in the volume more accurately.

  The pneumatic valve can be used in a variety of applications, for example:
  - To automatically vent gasses in a burn chamber based on control input
  - The filling of a volume quickly, based on a customizable control pressure
