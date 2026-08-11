# 穿梭机制造（EN 源文件）

> 条目ID: `ShuttleCraft` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Shuttle-craft

  Shuttle construction is straightforward, albeit rather expensive and hard to pull off within an hour.

  It's a good activity if you have a significant amount of spare time on your hands and want a bit of a challenge.

  ## Getting started
  Required parts:
  
  [[实体:Thruster]]
  [[实体:Gyroscope]]
  [[实体:ComputerShuttle]]
  [[实体:SubstationBasic]]
  [[实体:PortableGeneratorPacman]]
  
  
  [[实体:CableHVStack]]
  [[实体:CableMVStack]]
  [[实体:CableApcStack]]
  [[实体:APCBasic]]
  

  Optional parts:
  
  [[实体:AirCanister]]
  [[实体:LightTube]]
  [[实体:AirlockGlassShuttle]]
  [[实体:SMESBasic]]
  
  
  [[实体:MobCorgiIan]]
  [[实体:NuclearBomb]]
  

  ## Foundation
  For this step you'll need steel sheets, metal rods, and floor tiles (optional).

  
    [[实体:SheetSteel]]
    [[实体:PartRodMetal]]
  
  
    [[实体:FloorTileItemSteel]]
    [[实体:FloorTileItemDark]]
    [[实体:FloorTileItemWhite]]
  

  Head out into space with steel sheets and metal rods in hand and click on the edge of the station to place lattice.

  Place a line of lattice about 3-4 tiles away from the station, then start building a platform with lattice.

  Keep doing this until you have a platform that is at least 3x3 in size, which is connected to the station via a single lattice line.

  Once you're finished constructing the base of your shuttle, you can use wirecutters to snip the connecting lattice that joins your new ship and the station.

  This platform is considered a different grid from the station and thus will not have any gravity or be held in place by a station anchor — it can move around freely.

  You can expand your lattice platform further by clicking just off the edge with some rods in hand.

  ## Docking Ports
  Shuttle airlocks serve as docking ports, where ships can dock to stations safely.

  The orientation of docking ports is important, as it determines on which face the shuttle will dock.

  The little numb on the bottom of the docking port determines the direction of the docking port.

  
    [[实体:AirlockShuttle]]
    [[实体:AirlockGlassShuttle]]
  

  ## Directional Control
  From there, once you have the shape you want, bring out and install thrusters at the edges.

  
    
    
    
    
  

  It's a good idea to install four thrusters, one on each side of the platform, to ensure you can move in any direction.

  They must be pointing outward into space to function and will not fire if there's a tile in the way of the nozzle.
  You can rotate thrusters—even anchored ones—using either <span style="color:yellow">**[keybind="RotateObjectClockwise"]**</span> or <span style="color:yellow">**[keybind="RotateObjectCounterclockwise"]**</span> to rotate clockwise or counterclockwise.

  Thrusters can be disabled or enabled using <span style="color:yellow">**[keybind="Use"]**</span> with an empty hand or <span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span>.

  ## Rotational Control
  Now that you have directional control, you'll need to install a gyroscope to control your rotation.

  
    [[实体:Gyroscope]]
  
  The placement of the gyroscope is not as important as the thrusters, but it should be somewhere convenient for you to access and power.

  Note for large mass objects, you may need more than one gyroscope to rotate effectively.

  ## Power
  Now that you have all the systems in place, you'll need to power them.

  For small shuttles, a J.R.P.A.C.M.A.N.-type portable generator is a good choice. It provides straight LV power, so you don't have to worry about transformers.
  Fuel for the generator is also commonly found in maintenance tunnels.

  
    
      [[实体:PortableGeneratorJrPacman]]
    
    
      [[实体:WeldingFuelTankFull]]
    
  

  Some stations, however, provide much better generators and compact solutions like the Shuttle APU or the static generator.
  These output HV and will have to be stepped down to MV and LV.
  Luckily, these stations also usually provide wallmount substation boards for this purpose.

  
    
      [[实体:GeneratorWallmountAPU]]
    
    
      [[实体:GeneratorBasic15kW]]
    
    
      [[实体:SubstationWallBasic]]
    
  

  ## Piloting
  Finally, install the shuttle computer wherever it is convenient and ensure all your thrusters and gyroscopes are receiving power (remember to wire the MV and LV networks!).
  If they are, congratulations! You should have a functional shuttle!

  Making it livable and good-looking is left as an exercise to the reader.
