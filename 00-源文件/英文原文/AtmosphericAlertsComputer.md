# 大气警报计算机（EN 源文件）

> 条目ID: `AtmosphericAlertsComputer` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

﻿
  # Atmospheric Alerts Computer
  The Atmospheric Alerts Computer is a computer that shows information on all air alarms and fire alarms across the station.

  
    [[实体:ComputerAlert]]
  

  It is a useful tool for quickly identifying areas that require attention.

  The Atmospheric Alerts Computer is often found in Atmospherics, and is used by Atmospherics Technicians to monitor atmospheres across the entire station.
  However, it is also a good indicator for general engineers to gauge station damage.

  The computer displays lists of Air Alarms in <span style="color:orange">Warning</span> and <span style="color:red">Danger</span> levels. Additionally, the computer displays the location of all air alarms, color-coded based on their current status.

  Air alarms with the normal status are hidden by default.
  You can toggle the visibility of normal air alarms by adjusting the filters at the bottom of the interface.

  The map draws a box around the area that the air alarm is monitoring, which can help identify the area that is in danger.
  This box will change color based on the status of the air alarm.

  If an Air Alarm is unpowered, it is shown as greyed out on the list and on the map.

  Clicking on an air alarm on the list or on the map will show detailed information about the atmosphere in that area, which can help gauge the type of emergency that is occurring.

  A list of triggered [textlink="fire alarms" link="FireAndGasControl"] is also displayed on the Atmospheric Alerts Computer in a separate tab, which can be used to quickly identify areas that might be on fire.

  You can silence specific alarms (such as alarms that monitor burn chambers and freezers) by clicking on the alarm in the list and pressing the "Silence alerts" button.
  This will hide the alarm from the list, but it will still be visible on the map.
