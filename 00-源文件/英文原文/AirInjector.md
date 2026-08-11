# 空气注入器（EN 源文件）

> 条目ID: `AirInjector` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  #Air Injector
  The air injector is a special vent that forces gasses into the atmosphere it's exposed to.
  
    [[实体:GasOutletInjector]]
  
  It is primarily used to force gasses into high-pressure rooms like the station's [textlink="gas storage rooms" link="GasMiningAndStorage"] or a burn chamber.

  The air injector does not require [textlink="power" link="Power"] to function.

  The air injector will inject gasses into the atmosphere it's exposed to until the atmosphere reaches <span style="color:orange">[protodata="GasOutletInjector" comp="GasOutletInjector" member="MaxPressure"/] kPa</span>.

  The air injector's speed is proportional to the amount of gas in the injector.
