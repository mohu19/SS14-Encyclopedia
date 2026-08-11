# 反物质引擎（AME）（EN 源文件）

> 条目ID: `AME` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Antimatter Engine (AME)
  The Antimatter Engine is a short-term support generator for the station, providing a sizable chunk of power for a limited time.

  It's mainly used to assist engineers in starting up bigger engines like the [textlink="Singularity Engine" link="SingularityEngine"] or [textlink="Tesla Engine" link="TeslaEngine"], by supplementing the station's [textlink="batteries" link="PowerStorage"] with partial power to extend their runtime.

  ## Construction
  Required parts:
  
  [[实体:AmeController]]
  [[实体:AmePartFlatpack]]
  [[实体:AmeJar]]
  

  The AME Controller is the part of the AME that outputs power to the station's grid through an [textlink="HV connection" link="VoltageNetworks"].
  Because of this, you'll want to start your AME construction with the controller on top of an <span style="color:orange">HV wire</span>.

  Most stations have exposed <span style="color:orange">HV wiring</span> or designated spots to wrench an AME controller, so that it connects to the grid.

  AME shielding is the physical structure that makes the antimatter engine. It's made by converting AME flatpacks into shielding using a multitool.

  To construct an AME, start putting down a 3x3 or larger square of AME flatpacks in preparation for construction, making sure to maximize the number of "center" pieces that are surrounded on all eight sides.
  The greater amount of center pieces, the more cores your AME will have, and the more power it will be able to output safely.

  
    [[实体:AmePartFlatpack]]
    [[实体:AmePartFlatpack]]
    [[实体:AmePartFlatpack]]
  
  
    [[实体:AmePartFlatpack]]
    [[实体:AmePartFlatpack]]
    [[实体:AmePartFlatpack]]
  
  
    [[实体:AmePartFlatpack]]
    [[实体:AmePartFlatpack]]
    [[实体:AmePartFlatpack]]
  

  Once this is done, you can use a multitool to convert each AME flatpack into shielding, which should form a finished AME configuration.

  [[实体:AmeController]]
  
    
    
    
  
  
    
    
    
  
  
    
    
    
  
  
    <span style="color:#999999">[italic]An example of a one core setup[italic]</span>
  

  ## Operation
  To start the AME, insert a fuel jar into the AME controller, and set the safe injection rate.

  The safe injection rate is the point where the AME can safely run without overheating, while maximizing power output.

  This rate is always twice the core count.

  For example, an AME with one core will have a safe injection rate of 2. With two cores, the safe injection rate would be 4, and so on.

  Any more than this ratio will eventually result in the engine <span style="color:#ff0000">overheating</span> and, shortly afterwards, <span style="color:#ff0000">exploding</span>.

  The AME controller will [textlink="report" link="InspectingPower"] on both the amount of power it is providing to the grid, and the theoretical maximum power it could provide if demanded.
