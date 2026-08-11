# 奇点／特斯拉引擎（EN 源文件）

> 条目ID: `SingularityTeslaEngine` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Singularity / Tesla Engine

  The Singularity Engine / Tesla Engine can yield <span style="color:#a4885c">infinite power</span> for the entire shift, making it a valuable asset to the station.

  It can also <span style="color:red">destroy the whole station</span> with equal ease, and requires careful preparation and monitoring to prevent a **loose**.

  # Setting it up
  Both engines follow the same basic setup steps, but have different subsystems and requirements.

  ## Containment Field
  The Containment Field is a multi-tile beam field that repels the singularity or tesla, keeping it from escaping.

  The emitter lasers and the containment fields can also cause damage and/or cause you to be sent flying into deep space; <span style="color:#a4885c">avoid touching them</span> when active.

  
    [[实体:Emitter]]
    [[实体:ContainmentFieldGenerator]]
    [[实体:ContainmentField]]
  

  Containment Fields are generated between active Containment Field Generators, which are powered by emitters.

  A containment field generator can generate a containment field if:
  - The generator has been turned on,
  - another field generator is within 8 tiles,
  - and the field generators are on the same cardinal axis.

  This means that the maximum length of a containment field is 7 tiles.

  You can turn on a containment field generator by interacting with it using <span style="color:yellow">**[keybind="Use"]**</span>.
  Containment field generators won't work if they aren't turned on, even when struck by an emitter. Remember to turn on the field generator!

  The containment field generator has an internal energy level, which is filled by striking it with an emitter. When the containment field generator has enough stored energy, it will generate a containment field.

  This energy level will naturally decay over time, and the field will disappear when the energy level reaches zero after a delay.

  When the containment field is active, you cannot turn off the field generator or unanchor it. You must wait for the field to decay before you can turn off the generator.

  
    [[实体:ContainmentFieldGenerator]]
    
    
    
    [[实体:ContainmentFieldGenerator]]
  

  ## Emitters
  Emitters are the devices that power the containment field generators.

  
    [[实体:Emitter]]
  

  The emitters connect to MV cables, and fire lasers as long as they have power and are turned on.

  It is recommended to <span style="color:#a4885c">lock the emitters</span> with <span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span>, to prevent any break-in no-gooders from loosing the singularity or tesla by simply switching off the field.

  ## Particle Accelerator
  The Particle Accelerator (PA) is a multi-tile structure that launches accelerated particles from its emitters.

  
    
  

  
    
    
    
  

  
    
  

  
    
    
    
  

  Some stations already have an unfinished PA.
  To complete it, first ensure there is a MV cable beneath the PA power box, anchor all the parts, and then add an LV cable to each part.

  
    [[实体:CableApcStack]]
  

  Then use a screwdriver to screw back the panels.
  <span style="color:#a4885c">Scan parts</span> using the PA control computer to check if it's operational (the PA will not function if you do not scan it!).
  If it shows up as incomplete, examine what's missing.

  
    [[实体:ParticleAcceleratorControlBox]]
