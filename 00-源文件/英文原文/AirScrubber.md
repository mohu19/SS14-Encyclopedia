# 空气洗涤器（EN 源文件）

> 条目ID: `AirScrubber` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Air Scrubber
  The air scrubber is essential in maintaining an atmosphere free of waste gasses emitted by breathing creatures and atmospheric upsets.
  Its primary job is to scrub unwanted gasses from the atmosphere it's exposed to.
  
    [[实体:GasVentScrubber]]
  
  The air scrubber requires [textlink="power" link="Power"] through a nearby [textlink="LV cable" link="VoltageNetworks"] to function.

  The default behavior of an air scrubber is to scrub all gasses except Nitrogen and Oxygen from the atmosphere it's exposed to. It will continue this behavior unless directed by a [textlink="linked" link="Networking"] [textlink="air alarm" link="AirAlarms"].

  The scrubber can be welded with any welding tool to stop it from functioning.

  ## Configuration Options
  When [textlink="linked" link="Networking"] to an [textlink="air alarm" link="AirAlarms"], air scrubbers gain more functionality.

  The target gasses for scrubbing can be defined in the "Gas filters" dropdown. Keep in mind this resets if you change [textlink="air alarm" link="AirAlarms"] modes.

  Air scrubbers have two "direction" options: Scrubbing and Siphoning.
  - Scrubbing scrubs gasses as defined in the gas filters.
  - Siphoning ignores all gas filters, and sucks all gasses out of the atmosphere.

  Both of these modes are limited by the Rate setting, which defines the rate (in litres) at which the scrubber sucks gasses from its exposed atmosphere.

  Air scrubbers also have a "WideNet" setting, which expands the radius of the scrubber's operating range. Normally, the scrubber scrubs the atmosphere on the single tile it's exposed to.
  In WideNet mode, the scrubber scrubs gas from the 4 tiles surrounding the scrubber, as shown:

  
    [[实体:FloorTileItemSteel]]
  
  
    [[实体:FloorTileItemSteel]]
    [[实体:GasVentScrubber]]
    [[实体:FloorTileItemSteel]]
  
  
    [[实体:FloorTileItemSteel]]
  

  This effectively multiplies its total speed, as air scrubbers will now preform their scrubbing work on 5 tiles at once.

  Scrubbers [textlink="linked" link="Networking"] to an [textlink="air alarm" link="AirAlarms"] in auto mode will automatically enable WideNet mode under the [textlink="air alarm's" link="AirAlarms"] "Filtering (Wide)" mode when a high concentration of unwanted gasses is detected in the atmosphere.

  WideNet is extremely useful in quickly scrubbing large amounts of tritium from plasma burn chambers.
