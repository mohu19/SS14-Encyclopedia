# 权限配置器（EN 源文件）

> 条目ID: `AccessConfigurator` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Access Configurator
  The access configurator is a tool used to specify what type of personnel may use certain devices.

  
	  [[实体:AccessConfigurator]]
  

  Configurable devices can include airlocks, secure crates and lockers, as well as access restricted machines.
  Note: Airlocks can have their accesses configured by the <span style="color:#a4885c">Network Configurator</span> (or multitool), for convenience.

  ## Where to find Access Configurators
  Each station is equipped with up to two access configurators. The first is in the possession of the Chief Engineer, while the second can be found with the Head of Personnel.

  ## How to use the access configurator
  To modify a device using the access configurator:
  - First, use the access configurator on the chosen device to link them together. This will automatically open the configurator UI.
  - Next, insert an ID card into the access configurator.
  - Set the access requirements of the connected device. What requirements can be added or removed will depend upon the access privileges of the inserted ID card.
  - Any changes made will be applied <span style="color:#a4885c">immediately</span> - simply eject the ID card from the access configurator and close the UI when you are done.

  ## Restrictions on changing access
  As a safety precaution, the inserted ID must possess **all** of the access requirements that are currently active on the connected device in order to modify it.

  For example, a device which can be accessed by both 'Science' and 'Medical' personnel can only by modified using an ID card that has access to <span style="color:#a4885c">both</span> of these departments.
  The access configurator will warn the user if the inserted ID card does not have sufficient privileges to modify a device.

  A device with no access requirements set, like a public access airlock, can be modified using any valid station ID card.

  ## Repairing access-broken ID card readers
  Syndicate agents may attempt to hack access-restricted devices through the use of an <span style="color:#a4885c">Authentication Disruptor</span>.
  This nefarious tool will completely short out any ID card readers that are attached to the device, making it all-access.

  
    [[实体:AccessBreaker]]
  

  To repair the damage, you'll commonly need to partially deconstruct the device and reconstruct it.
  This will reset the access requirements to defaults, allowing you to reconfigure the device as needed.

  ## Repairing access-broken Airlocks
  Airlocks can be repaired multiple ways if their access requirements have been tampered with.

  If you have an Access Configurator, you can use a <span style="color:#a4885c">Screwdriver</span> to remove the airlock's maintenance panel, and then use the Access Configurator to reconfigure the airlock's access requirements.
  No partial deconstruction is needed.

  If you don't have an Access Configurator, you can still fix the airlock by partially deconstructing it until you remove the door electronics, and then reconstructing it.
  This will reset the airlock to the default access requirements it had at the start of the shift.
