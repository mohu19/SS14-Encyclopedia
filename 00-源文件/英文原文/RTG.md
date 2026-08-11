# RTG（EN 源文件）

> 条目ID: `RTG` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Radioisotope Thermoelectric Generator (RTG)

  
    [[实体:GeneratorRTG]]
  

  A Radioisotope Thermoelectric Generator (RTG) is a passive power source that generates power from the decay of radioactive isotopes.

  They require no maintenance and are a reliable source of power, making them ideal for powering essential systems that need to be online at all times, like Telecoms, the AI, or the Crew Monitoring Server.

  RTGs always generate <span style="color:orange">[protodata="GeneratorRTG" comp="PowerSupplier" member="MaxSupply" format="N0"/] W</span> of power and must be connected to an <span style="color:orange">HV power</span> [textlink="network" link="VoltageNetworks"] to function.

  However, they're only accessible through salvage finding one on an expedition. Should they bring some in, make sure to thank them!

  ## RTG Damage
  
    [[实体:GeneratorRTGDamaged]]
  
  If RTGs take enough damage, they can become damaged RTGs.
  Damaged RTGs behave just like regular ones, but they're <span style="color:yellow">radioactive</span>.

  That means they're more dangerous, but on the bright side, you can put radiation collectors next to them to turn that radiation into more power.
  This is usually more worthwhile, considering the power is still free, so long as you can find a safe spot to put the RTG(s) in.
