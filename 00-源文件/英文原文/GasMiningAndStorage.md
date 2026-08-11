# 气体开采与储存（EN 源文件）

> 条目ID: `GasMiningAndStorage` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Gas Mining and Storage
  Gasses are often permanently used. Whether they are lost to [textlink="space" link="Spacing"] or used in a burn chamber, the station needs to be able to produce more gas to replace what is lost.
  It also needs to store this gas in a safe and efficient manner.

  ## Gas Miners
  Gas miners are used to replenish the station's gas supply. They are found in the gas storage tanks in Atmospherics.

  
    [[实体:GasMinerOxygenStation]]
    [[实体:GasMinerNitrogenStation]]
  

  Gas miners constantly produce room temperature gas and push it into the exposed atmosphere. They require no power to function, and never stop working unless they have reached the defined **cutoff pressure**.

  You can see more information about the gas miners by inspecting them using <span style="color:yellow">**[keybind="ExamineEntity"]**</span>.
  Try inspecting the gas miners presented above.

  Gas miners come in tiers, with the larger versions having a higher pressure cutoff than the smaller versions.

  
    [[实体:GasMinerNitrogen]]
    [[实体:GasMinerNitrogenStation]]
    [[实体:GasMinerNitrogenStationLarge]]
  

  If gas miners are ever unanchored from the station, they can be reanchored using a regular wrench.

  ## Gas Storage
  Gas storage tanks are used to store gas produced by the gas miners, and to make it available to other processes. They are found in Atmospherics.

  
    
    
    
    
    
  
  
    
    
    
    
    
  
  
    
    
    
    
    
  

  
    <span style="color:#999999">[italic]An example of a small gas holding tank[italic]</span>
  

  Various atmos processes insert and remove gasses from the gas storage tanks.
  For example:
  - The gas miner provides fresh gasses to the gas storage tanks, if there is room.
  - The recyclernet injects reclaimed gasses into the gas storage tanks for reuse.
  - Setups like the distronet and burn chamber remove gasses from the gas storage tanks.

  Gas storage tanks are designed to be able to be measured using a [textlink="Gas Analyzer" link="AtmosTools"].
  Because the outflow vent is a [textlink="passive vent" link="PassiveVent"], you can use a [textlink="gas analyzer" link="AtmosTools"] to measure the gas content of the [textlink="pump's" link="Pumps"] input, which is drawing from the gas storage tank.
