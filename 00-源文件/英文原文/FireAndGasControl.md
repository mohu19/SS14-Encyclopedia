# 火灾与气体控制（EN 源文件）

> 条目ID: `FireAndGasControl` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Fire and Gas Control
  Unfortunately, [textlink="fires" link="Fires"], [textlink="spacing" link="Spacing"], and other [textlink="atmospheric upsets" link="AtmosphericUpsets"] are a common occurrence on the station.
  These upsets can quickly spread throughout the station and make the atmosphere uninhabitable for the crew.

  
    [[实体:Firelock]]
    [[实体:FirelockGlass]]
    [[实体:FirelockEdge]]
    [[实体:FireAlarm]]
  

  To combat this, stations have a variety of devices to help prevent these upsets from spreading.

  ## Firelocks
  Firelocks are a simple and effective way to prevent fires from spreading throughout the station.

  Based on conditions sensed by the firelock, or through instruction from a connected [textlink="air" link="AirAlarms"] or fire alarm, they can close off sections of the station to prevent the spread of dangerous conditions.

  ## Station Sectioning
  Firelocks are intentionally placed in key areas to divide the station into sections. Open spaces like hallways or promenades are divided into smaller sections. This prevents the spread of dangerous conditions to the entire station through connected rooms, hallways, and other open spaces.

  ## Basic Operation
  When not connected to an [textlink="air alarm" link="AirAlarms"] or fire alarm, firelocks will function based on the conditions they sense. Firelocks will drop (close) if:
  - The temperature between the two sides of the firelock is different by <span style="color:orange">[protodata="Firelock" comp="Firelock" member="TemperatureThreshold"/] K</span> or more.
  - The pressure between the two sides of the firelock is different by <span style="color:orange">[protodata="Firelock" comp="Firelock" member="PressureThreshold"/] kPa</span> or more.

  If these conditions continue, the firelock will enter lockout mode. Firelocks in lockout mode will have <span style="color:red">red</span> lights and cannot be pried open by hand. They can only be opened by people with Engineering access or by using a crowbar.

  Firelocks in lockout mode cannot be opened by using Engineering access if they are unpowered. Only a crowbar can open an unpowered firelock in lockout mode.

  If the conditions between the two sides of the firelock return to within acceptable differences, the firelock will disable lockout mode, and can be opened by anyone.
  Note that this only means that the conditions are the same on both sides of the firelock, not that they are safe.

  A common example of this is a firelock that has released due to both sides being exposed to space.

  ## Connecting to Air and Fire Alarms
  Firelocks can be connected to [textlink="air alarms" link="AirAlarms"] and fire alarms to receive instructions on when to drop.
  Firelocks use the [textlink="List system" link="Networking"], and you can connect these devices using a multitool or network configurator.

  
    [[实体:Firelock]]
    [[实体:Multitool]]
    [[实体:NetworkConfigurator]]
    [[实体:FireAlarm]]
    [[实体:AirAlarm]]
  

  Each firelock has its own unique address. The process for connecting air vents, scrubbers, and sensors to air alarms is very similar.

  ## Operation Under Air Alarms
  When connected to an air alarm, firelocks will also drop under the command of the connected [textlink="air alarm" link="AirAlarms"].

  Firelocks will drop if the air alarm reaches a <span style="color:red">Danger</span> alert state. Firelocks will remain dropped until the air alarm returns to a <span style="color:green">Green</span> alert state.

  Firelocks that are in lockout mode will not raise even if the air alarm returns to a <span style="color:green">Green</span> alert state. Even if the pressure difference is resolved, the firelock will remain dropped until the air alarm re-sends a green alert state.

  ## Operation Under Fire Alarms
  When connected to a fire alarm, firelocks will drop if the fire alarm is triggered. Firelocks will remain dropped until the fire alarm is reset.

  ## Fire Alarms
  Fire alarms are devices that can be used to centrally control all connected firelocks.

  
    [[实体:FireAlarm]]
  

  Devices with sensors can be [textlink="linked" link="Networking"] to fire alarms, which will trigger the fire alarm if the sensor enters the <span style="color:red">Danger</span> temperature threshold as defined by its sensors.

  When the fire alarm is triggered, all connected firelocks will be overridden with a <span style="color:red">Danger</span> alert state and will drop.

  The alarm will automatically clear itself when the sensor returns to a <span style="color:green">Normal</span> temperature threshold.

  You can trigger and reset a fire alarm manually by interacting with it.

  This can be used to quickly drop firelocks in a room manually, or to raise them after an upset has been resolved.
