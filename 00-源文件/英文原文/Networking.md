# 网络（EN 源文件）

> 条目ID: `Networking` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Networking
  On the station, devices need to communicate to each other to preform their functions.
  [textlink="Air alarms" link="AirAlarms"] need to talk to their respective devices, [textlink="doors" link="Airlocks"] need to be linked to form proper airlocks, and much more.

  This is done through two systems, the Link system and the List system.

  You can use either the Multitool or Network Configurator to interact with these systems.
  You can switch between the different systems using <span style="color:yellow">**[keybind="AltActivateItemInHand"]**</span> or by hovering your cursor over the device and using <span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span>.

  
    
      [[实体:Multitool]]
    
    
      [[实体:NetworkConfigurator]]
    
  

  Some devices will require access to link devices to them.
  For example, you need Atmospherics access to link devices to an [textlink="air alarm" link="AirAlarms"].
  For doors, you'll need the access level of the door you're linking to.

  ## Link System
  The link system is used for explicitly linking two devices, such as linking a door to another door.

  
    [[实体:AirlockExternal]]
    [[实体:AirlockEngineering]]
    [[实体:BlastDoor]]
    [[实体:SignalButton]]
  

  Under the link system, devices have **ports** that are capable of either sending or receiving signals.

  Hovering over a port using your cursor will show a tooltip that tells you what the port does.
  For example, output ports will state the conditions under which they will invoke a signal, and input ports will state what the device will do if it receives a signal.

  ## List System
  The list system is used for linking multiple devices to a single primary device, such as linking multiple atmospherics devices to an air alarm.

  
    [[实体:AirAlarm]]
    [[实体:GasVentPump]]
    [[实体:GasVentScrubber]]
    [[实体:AirSensor]]
    [[实体:Firelock]]
  

  Each device has its own unique address, which is used to identify it in the list system. When you link a device to a primary device, you are adding the device's address to a list of devices that the primary device will communicate with.

  You can save a device's address to your tool by interacting with the device using <span style="color:yellow">**[keybind="Use"]**</span>.

  Once you have a list of devices saved to your tool, you can link them to a primary device by interacting with the primary device using <span style="color:yellow">**[keybind="Use"]**</span>, which will bring up a UI.

  The UI has multiple options:
  - Set: Overwrites the current list of linked devices with the devices saved on the tool.
  - Add: Adds the devices saved on the tool to the current list of linked devices.
  - Clear: Removes all linked devices from the air alarm.
  - Copy: Copies the list of currently linked devices to the tool.
  - Show: Draws a line between the primary device and all linked devices. This is useful for visualizing the area the air alarm covers.

  If you need to clear your tool, you can press <span style="color:yellow">**[keybind="Use"]**</span> on the tool or use <span style="color:yellow">**[keybind="ActivateItemInHand"]**</span> to bring up a list of saved devices, and then press the "Clear" button.
