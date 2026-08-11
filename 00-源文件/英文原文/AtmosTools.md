# 大气工具（EN 源文件）

> 条目ID: `AtmosTools` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Atmos Tools
  Atmospheric Technicians have the same core toolset as Engineers, but they also have access to two new tools, the Holofan Projector and the Gas Analyzer.

  
    [[实体:HolofanProjector]]
    [[实体:GasAnalyzer]]
  

  ## Holofan Projector
  The Holofan Projector is a tool that can project a barrier of hard-light which blocks air and gas flow, while still allowing people to pass through.

  
    [[实体:HolofanProjector]]
    [[实体:HoloFan]]
  

  This is super useful for moving in between [textlink="firelock buffers" link="FireAndGasControl"] without leaking gas between rooms, as well a signifying to regular crew that a room may be unsafe for entry.
  It can also be used for forming a temporary barrier to allow crew to quickly move between a spaced and unspaced area without risk of leaking air from other rooms.

  It has an internal charge that will deplete with each use, but it can be recharged by taking out the power cell and inserting it into a cell charger or recharger.

  Holofans that are placed adjacent to a [textlink="firelock" link="FireAndGasControl"] will deactivate the firelock lockout, allowing the firelock to be opened by hand.

  ## Gas Analyzer
  The Gas Analyzer is a tool that can be used to analyze the gas composition of an exposed atmosphere, or any [textlink="atmospheric device" link="GasManipulation"] containing gas.

  
    [[实体:GasAnalyzer]]
  
  
    [[实体:GasPipeBend]]
    [[实体:GasPressurePump]]
    [[实体:SignalControlledValve]]
    [[实体:GasFilter]]
    [[实体:StorageCanister]]
    [[实体:GasThermoMachineFreezer]]
  

  You can use the Gas Analyzer by clicking on a gas-containing [textlink="device" link="GasManipulation"], or by clicking on the air in the room.

  When used, the gas analyzer will report on:
  - The volume of the device measured (not the volume of the gas!)
  - The total pressure of the gas, in kPa
  - The temperature of the gas, in Kelvin (K) and Celsius (C)
  - The precise composition of the gas in molar amounts, and as a percentage of the total gas volume

  At the bottom of the UI, the gas analyzer will display a visual indication of the different [textlink="gasses" link="Gasses"] present in the composition, as well as their relative concentrations.

  When the gas analyzer is analyzing binary and trinary [textlink="devices" link="GasManipulation"] (devices with two and three inputs/outputs), it will display the composition of each input/output separately. This is useful for troubleshooting gas [textlink="mixing and filtering" link="MixingAndFiltering"] setups.
