# 温控机（EN 源文件）

> 条目ID: `Thermomachines` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Thermomachines
  Thermomachines are devices that manipulate the temperature of gasses within a [textlink="pipe network" link="PipeNetworks"] or exposed atmosphere.
  
    [[实体:SpaceHeater]]
    [[实体:GasThermoMachineHeater]]
    [[实体:GasThermoMachineFreezer]]
  
  They are essential for maintaining the temperature of gasses for various applications.

  All thermomachines work by using [textlink="electrical power" link="Power"] to heat or cool the atmosphere.
  How much they heat/cool the atmosphere is directly related to the amount of power they consume.

  Thermomachines also have an efficiency coefficient, which determines how much they can heat or cool the atmosphere per unit of power consumed.

  To prevent overshooting their target value, thermomachines will scale back their heating/cooling power as they approach the target temperature.
  However, they will still consume the same amount of electrical power, even when idle.

  All thermomachines have a target temperature tolerance of <span style="color:orange">[protodata="GasThermoMachineFreezer" comp="GasThermoMachine" member="TemperatureTolerance"/] K</span>, meaning they will stop heating or cooling when the temperature is within <span style="color:orange">[protodata="GasThermoMachineFreezer" comp="GasThermoMachine" member="TemperatureTolerance"/] K</span> of the target temperature.

  ## Space Heater
  The space heater is a portable temperature control unit that heats or cools gas in the atmosphere it's exposed to.
  It's a simple and effective way to maintain the temperature of a room, without having to build a pipenet or other system.

  
    [[实体:SpaceHeater]]
  

  They can be commonly found in Atmospherics, although the relevant machine board can be printed at a circuit imprinter, commonly found in Science.

  The space heater can cool to as low as <span style="color:orange">[protodata="SpaceHeater" comp="SpaceHeater" member="MinTemperature"/] K</span> and heat to as high as <span style="color:orange">[protodata="SpaceHeater" comp="SpaceHeater" member="MaxTemperature"/] K</span>.

  It also has three power settings which determine how fast it heats or cools the atmosphere.

  Botany or science will often request these to maintain the temperature of their plants or department.

  ## Pipenet Thermomachines (Freezer and Heater)
  Pipenet thermomachines are more powerful stationary temperature control units that can be used to heat or cool gas in a [textlink="pipenet." link="PipeNetworks"]

  
    [[实体:GasThermoMachineHeater]]
    [[实体:GasThermoMachineFreezer]]
  

  They draw <span style="color:orange">[protodata="GasThermoMachineFreezer" comp="GasThermoMachine" member="HeatCapacity" format="N0"/] W</span> of power and can heat or cool gas in a pipenet to as high as <span style="color:orange">[protodata="GasThermoMachineFreezer" comp="GasThermoMachine" member="MaxTemperature"/] K</span> or as low as <span style="color:orange">[protodata="GasThermoMachineFreezer" comp="GasThermoMachine" member="MinTemperature"/] K</span>.

  You can swap the mode of the thermomachine by deconstructing it and using a screwdriver on its circuit board.
  The board can be printed at a circuit imprinter, commonly found in Science.

  
    [[实体:GasThermoMachineFreezer]]
    [[实体:MachineFrame]]
    [[实体:ThermomachineFreezerMachineCircuitBoard]]
    [[实体:Screwdriver]]
    [[实体:ThermomachineHeaterMachineCircuitBoard]]
    [[实体:MachineFrame]]
    [[实体:GasThermoMachineHeater]]

  

  ## Thermomachines from Hell
  Science can research more powerful thermomachines, aptly called hellfire heaters and freezers.
  These machines are much more powerful than their standard counterparts, but they also consume more power.

  
    [[实体:GasThermoMachineHellfireHeater]]
    [[实体:GasThermoMachineHellfireFreezer]]
  

  These machines draw <span style="color:orange">[protodata="GasThermoMachineHellfireFreezer" comp="GasThermoMachine" member="HeatCapacity" format="N0"/] W</span> of power and can heat or cool gas in a pipenet to as high as <span style="color:orange">[protodata="GasThermoMachineHellfireFreezer" comp="GasThermoMachine" member="MaxTemperature"/] K</span> or as low as <span style="color:orange">[protodata="GasThermoMachineHellfireFreezer" comp="GasThermoMachine" member="MinTemperature"/] K</span>.

  However, they also leak <span style="color:orange">[protodata="GasThermoMachineHellfireFreezer" comp="GasThermoMachine" member="EnergyLeakPercentage" format="P0"/]</span> of their energy to the surrounding environment, heating or cooling the exposed atmosphere respectively.
  This can be dangerous if not properly managed.
