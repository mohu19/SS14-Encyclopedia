# 电力储存（EN 源文件）

> 条目ID: `PowerStorage` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Power Storage
  Because of [textlink="Power Ramping" link="Ramping"], it is important to have power storage devices to help flatten out spikes and dips in power usage, as well as to provide power in the event of a power deficit.

  Each transformer for its respective power level (<span style="color:orange">HV</span>, <span style="color:yellow">MV</span>, and <span style="color:green">LV</span>) has an attached small battery to handle minor spikes and dips; however, this is not viable in the case of a large grid deficit.

  ## SMES

  The Superconducting Magnetic Energy Storage (SMES) unit is a device that can store a large amount of power and release it quickly.

  
    [[实体:SMESBasic]]
  

  In order to charge the SMES unit, <span style="color:orange">HV</span> power must be provided to a cable terminal pointing at the SMES unit. The SMES will draw power from the terminal and send power out from underneath.

  The terminal will ensure that the <span style="color:orange">HV input</span> and <span style="color:orange">HV output</span> do not connect.

  
    
      [[实体:CableTerminal]]
    

    
      [[实体:CableHV]]
      
      
      [[实体:CableHV]]
    
  

  SMESes can store <span style="color:orange">[protodata="SMESBasic" comp="Battery" member="MaxCharge" format="N0"/] J</span> of energy and can output a maximum <span style="color:orange">[protodata="SMESBasic" comp="PowerNetworkBattery" member="MaxSupply" format="N0"/] W</span> of power.

  If the battery is full, the SMES will pass through the power it receives from the input cable to the output cable. In the event of a power deficit, the SMES will ramp up to supplement the power draw.

  ## Advanced SMES
  The Advanced SMES unit is a more advanced version of the SMES unit that can store even more power.

  
    [[实体:SMESAdvanced]]
  

  They're primarily used in station SMES arrays to store large amounts of power for the station's power grid.
  They help to buy engineers time to setup power at roundstart or to provide power in the event of a power deficit for extended periods of time.

  Advanced SMESes can store <span style="color:orange">[protodata="SMESAdvanced" comp="Battery" member="MaxCharge" format="N0"/] J</span> of energy and can output a maximum <span style="color:orange">[protodata="SMESAdvanced" comp="PowerNetworkBattery" member="MaxSupply" format="N0"/] W</span> of power.

  Keep in mind that these aren't a magic solution to power deficits and they can't store infinite energy.
  A station load will drain these battries quickly if there is no power source partially supporting them.
