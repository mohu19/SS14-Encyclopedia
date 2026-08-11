# 便携式发电机（EN 源文件）

> 条目ID: `PortableGenerator` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Portable Generators

  The "P.A.C.M.A.N." line of portable generators are used to provide emergency or supplemental power to key rooms, areas, or even departments.
  They are easy to set up and maintain, and can be used to power critical systems and areas in the event of a power outage.

  
    [[实体:PortableGeneratorJrPacman]]
    [[实体:PortableGeneratorPacman]]
    [[实体:PortableGeneratorSuperPacman]]
  

  # The Junior

  
    [[实体:PortableGeneratorJrPacman]]
    [[实体:WeldingFuelTank]]
  

  The J.R.P.A.C.M.A.N. can be found across the station in maintenance shafts, and is ideal for crew to set up themselves whenever there are power issues.
  Its output of up to <span style="color:orange">[protodata="PortableGeneratorJrPacman" comp="FuelGenerator" member="MaxTargetPower" format="N0"/] W</span> is enough to power a room or two, which can prove invaluable in a place like Medbay or Chemistry in the Medical Department.

  Setup is incredibly easy: wrench it down above an <span style="color:green">LV</span> power cable, give it some welding fuel, and start it up.

  Welding fuel is the only fuel source the J.R.P.A.C.M.A.N. can use and it can be found in welding fuel tanks across the station, commonly in maintenance areas.

  # The Big Ones

  
    [[实体:PortableGeneratorPacman]]
    [[实体:SheetPlasma]]
  

  
    [[实体:PortableGeneratorSuperPacman]]
    [[实体:SheetUranium]]
  

  The P.A.C.M.A.N. and S.U.P.E.R.P.A.C.M.A.N. is intended for usage by engineering for larger power outages and supplementing power in the event of a deficit.
  Bootstrapping larger [textlink="engines" link="SingularityTeslaEngine"], powering departments, and so on.

  The S.U.P.E.R.P.A.C.M.A.N. boasts a larger power output (up to <span style="color:orange">[protodata="PortableGeneratorSuperPacman" comp="FuelGenerator" member="MaxTargetPower" format="N0"/] W</span>) and longer runtime at maximum output, but scales down to lower outputs less efficiently.

  They connect directly to <span style="color:yellow">MV</span> or <span style="color:orange">HV</span> [textlink="power cables" link="VoltageNetworks"] and are able to switch between them for flexibility.

  The S.U.P.E.R.P.A.C.M.A.N and P.A.C.M.A.N require uranium sheets and plasma sheets as fuel, respectively.
