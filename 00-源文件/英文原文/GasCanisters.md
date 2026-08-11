# 储气罐（EN 源文件）

> 条目ID: `GasCanisters` ｜ 来源层: official ｜ 分类: engineering
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Gas Canisters
  
    [[实体:AirCanister]]
    [[实体:OxygenCanister]]
    [[实体:NitrogenCanister]]
  
  
    [[实体:CarbonDioxideCanister]]
    [[实体:StorageCanister]]
    [[实体:GasPort]]
  

  Gas canisters are a way to store gas in a portable container for easy transport.
  They can store <span style="color:orange">[protodata="StorageCanister" comp="GasCanister" member="Volume"/] liters</span> of gas.

  You can connect handheld tanks to a gas canister to refill them using the release valve on the canister.
  The release valve also has a adjustable pressure regulator to control the pressure of the handheld tank connected.

  Opening the release valve on a canister with no handheld tank connected will release gas into the atmosphere, at the specified regulator pressure.

  **Be sure to close the release valve before you eject your handheld tank!**

  ## Connector Ports
  Gas canisters and [textlink="portable scrubbers" link="PortableScrubber"] can be connected to a [textlink="pipenet" link="PipeNetworks"] by anchoring (wrenching) the device on top of a connector.
  When connected, gas will be free to move in and out of the canister to balance pressure, temperature, and composition.

  A pump can be used to insert or extract gas from a canister, useful for filling or emptying a canister entirely.
