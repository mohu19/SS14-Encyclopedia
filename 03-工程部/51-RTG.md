# RTG

> 条目ID: `RTG` ｜ 来源层: 官方 ｜ 分类: 03-工程部

---

> AI翻译



[RTG 热电发电机](00-实体清单/Structures.md)



放射性同位素热电发电机（RTG）是一种被动电源，通过放射性同位素的衰变产生电力。

它们无需维护，是可靠的电源，非常适合为需要始终在线的关键系统供电，如电信、AI 或船员监控服务器。

RTG 始终产生 <span style="color:orange">[protodata="GeneratorRTG" comp="PowerSupplier" member="MaxSupply" format="N0"/] W</span> 的电力，并且必须连接到<span style="color:orange">HV 电力</span>[网络](62-电压网络.md)才能运行。

不过，只有打捞队在远征中找到它们才能获得。如果他们带回来一些，记得好好感谢他们！

## RTG 损坏



[受损的 RTG](00-实体清单/Structures.md)



如果 RTG 受到足够的伤害，就会变成损坏的 RTG。
损坏的 RTG 与普通 RTG 行为相同，但具有<span style="color:yellow">放射性</span>。

这意味着它们更危险，但好的一面是，你可以在它们旁边放置辐射收集器，把辐射转化为更多电力。
考虑到电力仍然是免费的，只要你为 RTG 找到一个安全的放置位置，这样做通常更划算。
