# 大型炸弹拆除（EN 源文件）

> 条目ID: `Defusal` ｜ 来源层: official ｜ 分类: security
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Large Bomb Defusal
  So, you found a large bomb and it's beeping. These bombs take a long time to detonate and punch a big hole into the hull. Just keep reading, and nobody will explode.

  ## Gear
  You require two essential tools to perform defusal, however, a multitool is extremely helpful in terms of identifying wires.
  
    [[实体:Wirecutter]]
    [[实体:Screwdriver]]
    [[实体:Multitool]]
  

  For protective equipment, a <span style="color:yellow">bomb suit</span> or any other protective equipment can assist you in not blowing into gibs.
  
    [[实体:ClothingHeadHelmetBombSuit]]
    [[实体:ClothingOuterSuitBomb]]
    [[实体:ClothingOuterHardsuitRd]]
    [[实体:ClothingOuterHardsuitAtmos]]
  

  ## Hardbombs
  Listed below are the two common types of bombs you will encounter while defusing. A training bomb will only provide minor hull damage and generally not kill you. A syndicate bomb however will punch a big hole into the hull, and gib you if you are not wearing protective gear.
  
    [[实体:SyndicateBomb]]
    [[实体:TrainingBomb]]
  

  ## Arming
  To arm a bomb, you can either <span style="color:yellow">right click</span> and click <span style="color:yellow">Begin countdown[/click], or [color=yellow]alt-click</span> the bomb. It will begin beeping.

  ## Time
  A bomb has a limited time, at a minimum of [protodata="SyndicateBomb" comp="TimerTrigger" member="ShortestDelayOption"/] seconds and a maximum of [protodata="SyndicateBomb" comp="TimerTrigger" member="LongestDelayOption"/] seconds. You can view the timer by examining it, unless the Proceed wire is cut. Once the timer hits zero, the bomb will detonate.

  ## Bolts
  By default, once armed, a bomb will bolt itself to the ground. You must find the BOLT wire and cut it to disable the bolts, after which you can unwrench it and throw it into space.

  ## Wires
  You must access the wiring in order to defuse a bomb. You can use a <span style="color:yellow">screwdriver</span> to open the access panel. Inside, you will find many types of wires. In a standard syndicate bomb, there are around <span style="color:yellow">10 wires</span>, 3 are dummy wires, <span style="color:red">3 will cause a detonation</span>, and the rest that weren't mentioned can be found below (alongside BOOM wires). With each wire, you can do 3 actions. You can:
  - <span style="color:yellow">Pulse the wire</span> with a multitool, this can help you safely identify most wires.
  - <span style="color:red">Cut the wire</span> with a wirecutter, this can trigger various effects, be cautious of cutting without reason!
  - <span style="color:green">Mend the wire</span> with a wirecutter, this can restore some functionality of the bomb if it isn't disposable.

  Onward for the types of wires.

  ## Wire Types
  <span style="color:#a4885c">Activation Wire (LIVE)</span>
  - <span style="color:yellow">Pulse the wire</span>: Pulsing the wire will make the wire chirp and delay the bomb by 30 seconds.
  - <span style="color:red">Cut the wire</span>: Cutting the wire will defuse the bomb if active, otherwise, will begin the timer.
  - <span style="color:green">Mend the wire</span>: Nothing.

  <span style="color:#a4885c">Proceed Wire (PRCD)</span>
  - <span style="color:yellow">Pulse the wire</span>: Pulsing the wire will forward the time by 15 seconds.
  - <span style="color:red">Cut the wire</span>: Cutting the wire will disable the timer display on examine.
  - <span style="color:green">Mend the wire</span>: Nothing.

  <span style="color:#a4885c">Delay Wire (DLAY)</span>
  - <span style="color:yellow">Pulse the wire</span>: Pulsing the delay wire will delay the bomb by 30 seconds.
  - <span style="color:red">Cut the wire</span>: Nothing.
  - <span style="color:green">Mend the wire</span>: Nothing.

  <span style="color:#a4885c">Boom Wire (BOOM)</span>
  - <span style="color:yellow">Pulse the wire</span>: <span style="color:red">The bomb will explode if armed!</span>
  - <span style="color:red">Cut the wire</span>: <span style="color:red">The bomb will explode if armed!</span> Otherwise, will disable the bomb.
  - <span style="color:green">Mend the wire</span>: Re-enables the bomb if disabled previously.

  <span style="color:#a4885c">Bolt Wire (BOLT)</span>
  - <span style="color:yellow">Pulse the wire</span>: Pulsing the wire will make the bolts spin.
  - <span style="color:red">Cut the wire</span>: Cutting the wire will disable the bolts, throw it into space!
  - <span style="color:green">Mend the wire</span>: Mending the wire will re-enable the bolts.

  <span style="color:#a4885c">Dummy Wire</span>
  - Dummy wires don't do anything. You can pulse, cut, and mend them freely without affecting the bomb at all.
