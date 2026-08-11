# 电压网络（EN 源文件）

> 条目ID: `VoltageNetworks` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Voltage Networks
  In Space Station 14, power distribution is divided into three separate voltage networks.
  These networks are the <span style="color:green">Low Voltage</span> Network, the [color=Yellow]Medium Voltage[/color] Network, and the <span style="color:orange">High Voltage</span> Network.

  These networks power different types of machinery on the station.

  
    [[实体:CableHVStack]]
    [[实体:CableMVStack]]
    [[实体:CableApcStack]]
  

  ## Low Voltage Network
  The <span style="color:green">Low Voltage</span> Network is used for powering almost all small machines on the station. This includes things like lights, computers, and other small devices.

  
    [[实体:PoweredSmallLight]]
    [[实体:ComputerShuttleCargo]]
    [[实体:ComputerComms]]
    [[实体:Autolathe]]
    [[实体:VendingMachineEngivend]]
    [[实体:VendingMachineMedical]]
    [[实体:AlwaysPoweredWallLight]]
  

  <span style="color:green">Low Voltage</span> power is provided by APCs, which are wall-mounted devices that convert power from the [color=Yellow]Medium Voltage[/color] Network to <span style="color:green">Low Voltage</span>.

  
    [[实体:APCBasic]]
  

  <span style="color:green">Low Voltage</span> wire doesn't have to be directly run to every machine, as it can power multiple machines as long as the wire is close enough to the machine.
  It can power machines within 2 tiles radially, and 3 tiles in each cardinal direction.

  ## Medium Voltage Network
  The [color=Yellow]Medium Voltage[/color] Network is used for powering APCs and other power-hungry machinery that can only accept [color=Yellow]Medium Voltage[/color] power.
  The Particle Accelerator is an example, as it operates on [color=Yellow]Medium Voltage[/color] power.

  
    
  

  
    
    
    
  

  
    
  

  
    
    
    
  

  
    <span style="color:#999999">[italic]The Particle Accelerator[italic]</span>
  

  [color=Yellow]Medium Voltage[/color] power is provided by Substations, which are large machines that convert power from the [color=Orange]High Voltage[/color] Network to [color=Yellow]Medium Voltage[/color].

  There are also wallmount variants of these substations for compact spaces, like shuttles.
  
    
      [[实体:SubstationBasic]]
    
    
      [[实体:SubstationWallBasic]]
    
  

  ## High Voltage Network
  The [color=Orange]High Voltage[/color] Network is used for moving large amount of power across the station. It is used to power most power handling equipment, such as SMES units and Substations.

  Most high-output generators output power to the [color=Orange]High Voltage[/color] Network.

  
    [[实体:SMESBasic]]
    [[实体:RadiationCollector]]
    [[实体:TeslaCoil]]
    [[实体:SubstationBasic]]
  

  ## Shock Damage
  If you are shocked by a cable carrying power, you will take damage. The amount of damage you take is based on the voltage of the cable that shocked you.

  <span style="color:green">Low Voltage</span> cables will deal less damage than [color=Yellow]Medium Voltage[/color] cables, which will deal less damage than [color=Orange]High Voltage[/color] cables.

  Energized [color=Orange]High Voltage[/color] and [color=Yellow]Medium Voltage[/color] cabling hurts, so be sure to wear insulated gloves when working with it.
