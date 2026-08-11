# 压差（EN 源文件）

> 条目ID: `DeltaPressure` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Delta Pressure
  Delta Pressure, or ΔP, is the difference in pressure between two areas.
  This difference in pressure can exert a force on objects between the two areas, dealing **pressure damage** to some objects in its way.

  Various objects made out of glass, such as Windows, Windoors, and Shutters can experience pressure damage if the ΔP between the two sides is high enough.
  This damage can cause these objects to shatter, allowing gas to flow freely between the two areas.

  Different types of objects have different thresholds for how much ΔP they can withstand before shattering.
  Generally, the stronger the glass, the higher the threshold. Objects that are thin will also have lower thresholds.

  Objects like walls, airlocks, and firelocks are not affected by ΔP.

  ## Standard Glass and Objects
  
    [[实体:Window]]
    [[实体:WindowDirectional]]
    [[实体:Windoor]]
    [[实体:ShuttersWindow]]
    [[实体:InflatableWall]]
  

  Standard full-size glass and other weak objects can withstand a ΔP of up to <span style="color:orange">[protodata="Window" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  Quarter-size glass, such as directional windows, can withstand a ΔP of up to <span style="color:orange">[protodata="WindowDirectional" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  ## Reinforced Glass and Objects
  
    [[实体:ReinforcedWindow]]
    [[实体:WindowReinforcedDirectional]]
    [[实体:WindoorSecure]]
    [[实体:ShuttleWindow]]
  

  Reinforced full-size glass can withstand a ΔP of up to <span style="color:orange">[protodata="ReinforcedWindow" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  Reinforced quarter-size glass can withstand a ΔP of up to <span style="color:orange">[protodata="WindowReinforcedDirectional" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  ## Plasma/Uranium Glass
  
    [[实体:PlasmaWindow]]
    [[实体:PlasmaWindowDirectional]]
    [[实体:WindoorPlasma]]
    [[实体:UraniumWindow]]
    [[实体:UraniumWindowDirectional]]
    [[实体:WindoorUranium]]
  

  Plasma glass and uranium glass can withstand a ΔP of up to <span style="color:orange">[protodata="PlasmaWindow" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  Plasma and uranium quarter-size glass can withstand a ΔP of up to <span style="color:orange">[protodata="PlasmaWindowDirectional" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  ## Reinforced Plasma/Uranium Glass

  
    [[实体:ReinforcedPlasmaWindow]]
    [[实体:PlasmaReinforcedWindowDirectional]]
    [[实体:WindoorSecurePlasma]]
    [[实体:ReinforcedUraniumWindow]]
    [[实体:UraniumReinforcedWindowDirectional]]
    [[实体:WindoorSecureUranium]]

  

  Reinforced plasma glass and uranium glass can withstand a ΔP of up to <span style="color:orange">[protodata="ReinforcedPlasmaWindow" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.

  Reinforced plasma and uranium quarter-size glass can withstand a ΔP of up to <span style="color:orange">[protodata="PlasmaReinforcedWindowDirectional" comp="DeltaPressure" member="MinPressureDelta"/] kPa</span> before starting to crack.
