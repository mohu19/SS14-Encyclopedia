# 气闸门（EN 源文件）

> 条目ID: `Airlocks` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Airlocks
  Airlocks are used to control access to different areas of the station.

  
    [[实体:Airlock]]
    [[实体:AirlockGlass]]
  

  Airlocks can be opened using either <span style="color:yellow">**[keybind="Use"]**</span> with an empty hand, <span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span> if hands are full, or by colliding with the airlock.

  Airlocks will only open if you have an ID card with the correct access level.
  The ID card must be in your hand or in your ID slot.
  In the case of having multiple IDs, the airlock will check them all when you try to open it.
  This behavior is also the same for IDs in a PDA.

  The access level required to open the door can be modified using an Access Configurator, or by using a Multitool on the door electronics for the airlock (which requires deconstruction).

  
    [[实体:AccessConfigurator]]
    [[实体:Multitool]]
    [[实体:DoorElectronics]]
  

  Airlocks block gas flow, so they can be used to seal off areas in case of a [textlink="hull breach" link="Spacing"] or a [textlink="fire." link="Fires"]
  They also store gas on their tile, even when closed, so be careful when opening them during or after a gas leak.

  ## Bolting and Emergency Access
  Airlocks can be bolted to prevent them from being opened or pried open by hand. When this occurs, the airlock will display red lights on the top of the door.

  Airlocks can also be set to emergency access. In this mode, anyone can open the airlock, regardless of access level. When this occurs, the airlock will display flashing yellow lights on the top of the door.

  ## Remote Control
  Airlocks can be controlled remotely, either by the station AI or by using a Door Remote.
  
    [[实体:PlayerStationAiEmpty]]
  
  
    <span style="color:#999999">[italic]The Station AI, which has remote control over all airlocks[italic]</span>
  

  
    [[实体:DoorRemoteEngineering]]
    [[实体:DoorRemoteCommand]]
    [[实体:DoorRemoteMedical]]
    [[实体:DoorRemoteService]]
    [[实体:DoorRemoteSecurity]]
    [[实体:DoorRemoteResearch]]
  
  
    <span style="color:#999999">[italic]Precious door remotes. With unlimited power...[italic]</span>
  


  Department heads usually get door remotes for their respective department.

  They can open, close, bolt, and set to emergency access using these remotes.

  ## Linking
  Airlocks can be linked using the [textlink="Link" link="Networking"] system to other devices.
  This allows for proper station airlocks to space, or to link multiple airlocks together.

  ## Styling
  Airlocks can come in different styles to match station departments. The department style commonly reflects the required access level.

  
    [[实体:Airlock]]
    [[实体:AirlockCargo]]
    [[实体:AirlockCommand]]
    [[实体:AirlockEngineering]]
    [[实体:AirlockMedical]]
    [[实体:AirlockScience]]
    [[实体:AirlockSecurity]]
  
  
    [[实体:AirlockGlass]]
    [[实体:AirlockCargoGlass]]
    [[实体:AirlockCommandGlass]]
    [[实体:AirlockEngineeringGlass]]
    [[实体:AirlockMedicalGlass]]
    [[实体:AirlockScienceGlass]]
    [[实体:AirlockSecurityGlass]]
  

  Airlocks can be repainted using a spray painter.
  
    [[实体:SprayPainter]]
  

  ## Wiring
  Airlocks have internal wiring under their maintenance panel, which can be opened using a screwdriver.
  Each wire controls some aspect of the airlock's functionality.
  When you either pulse, cut, or mend the wire, it will affect the airlock in different ways.

  The lights next to the wires will indicate the status of the wire:
  - A steady light indicates that the system is functioning as normal.
  - A flashing light indicates that the system is malfunctioning. It is either not working or is behaving not as intended.
  - No light indicates that the system is not powered.

  Below is a list of the wires and their functions:

  <span style="color:#a4885c">Bolt Wire (BOLT)</span>
  - <span style="color:yellow">Pulse the wire</span>: Bolts or unbolts the door.
  - <span style="color:red">Cut the wire</span>: Bolts the door.
  - <span style="color:green">Mend the wire</span>: Does nothing.

  <span style="color:#a4885c">Power Wire (POWR)</span>
  - <span style="color:yellow">Pulse the wire</span>: Cuts power to the door for a short time.
  - <span style="color:red">Cut the wire</span>: Either cuts power to the door if both power wires are cut, or causes a short circuit if only one is cut, shocking people without insulated gloves.
  - <span style="color:green">Mend the wire</span>: Either restores power to the door if both power wires are cut, or stops the short circuit if only one is cut.

  <span style="color:#a4885c">Log Wire (LOG)</span>
  - <span style="color:yellow">Pulse the wire</span>: Temporary disables door logging.
  - <span style="color:red">Cut the wire</span>: Disables door logging.
  - <span style="color:green">Mend the wire</span>: Re-enables door logging.

  <span style="color:#a4885c">Bolt Light (BLIT)</span>
  - <span style="color:yellow">Pulse the wire</span>: Turns the system off temporarily, or turns it back on.
  - <span style="color:red">Cut the wire</span>: Prevents the bolt light from turning on, which communicates if the door is bolted or not.
  - <span style="color:green">Mend the wire</span>: Turns the system back on.

  <span style="color:#a4885c">Timer Light (TIMR)</span>
  - <span style="color:yellow">Pulse the wire</span>: Reduces the door timer temporarily.
  - <span style="color:red">Cut the wire</span>: Disables the timer. The door will close as soon as it is safe to do so.
  - <span style="color:green">Mend the wire</span>: Re-enables the timer.

  <span style="color:#a4885c">Safety Light (SAFE)</span>
  - <span style="color:yellow">Pulse the wire</span>: Disables the safety system temporarily.
  - <span style="color:red">Cut the wire</span>: Disables the safety system. The door will close even if there is an obstruction.
  - <span style="color:green">Mend the wire</span>: Re-enables the safety system.

  <span style="color:#a4885c">AI Access Light (AIA)</span>
  - <span style="color:yellow">Pulse the wire</span>: Does nothing.
  - <span style="color:red">Cut the wire</span>: Disables AI access. The AI can no longer control the door.
  - <span style="color:green">Mend the wire</span>: Re-enables AI access.
