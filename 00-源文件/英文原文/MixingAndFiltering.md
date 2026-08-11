# 混合与过滤（EN 源文件）

> 条目ID: `MixingAndFiltering` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Mixing and Filtering
  Gas mixers and filters are essential tools for manipulating the composition of gasses within a [textlink="pipe network" link="PipeNetworks"].
  
    [[实体:GasMixer]]
    [[实体:GasFilter]]
  

  ## Gas Mixer
  Gas mixers are used to combine gasses in specific ratios within a [textlink="pipe network." link="PipeNetworks"]
  They are essential for creating controlled gas mixtures for various applications.

  Gas mixers have 3 connections: 2 inputs and 1 output, as shown below:
  
    
    
    
  

  [[实体:GasPipeStraight]]


  Gas mixers will still respect the requested gas mixture even if one of the input gasses is not available. For example:
  - If the requested mixture is 22% oxygen and 78% nitrogen, but there is no available oxygen, the mixer will not work until oxygen is available.
  - If oxygen is available, but at a pressure lower than required to create the proper mixture at the requested pressure, the mixer will still create the mixture, but the output will be at a lower pressure than requested.

  Gas mixers also mix gasses based on pressure, not on mols. This can cause problems if the gasses are at different temperatures. For example:
  - Presume a gas mixer was asked to mix Oxygen and Nitrogen at a ratio of 1:2 at a certain pressure.
  - The Nitrogen in this case is double the temperature of the Oxygen.
  - Hotter gas has more pressure, and thus fewer mols per volume than Oxygen.
  - Because of this, Nitrogen will have half the mols compared to Oxygen when the gas mixer attempts to create the mix.
  - The output will be 1:1 instead of 1:2. You'll have 1 mol of Nitrogen per 1 mol of Oxygen, instead of 2 mols of Nitrogen per 1 mol of Oxygen.

  Gas mixers can be used in a variety of applications, for example:
  - Mixing oxygen and nitrogen to create a breathable atmosphere
  - Mixing oxygen and plasma for plasma burning to create Tritium

  ## Gas Filter
  Gas filters are used to separate gasses from a mixture within a [textlink="pipe network." link="PipeNetworks"]

  
    
    
    
  
  
    [[实体:GasPipeStraight]]
  

  Gas filters will become blocked and will not filter gas if either output is blocked.

  Gas filters can be used in a variety of applications, for example:
  - Filtering out unwanted gasses from a [textlink="pipe network" link="PipeNetworks"]
  - Separating specific gasses for storage in a station's recyclernet
