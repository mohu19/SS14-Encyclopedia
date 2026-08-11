# 操作（EN 源文件）

> 条目ID: `Controls` ｜ 来源层: official ｜ 分类: newplayer
> 翻译提示：保留全部数值/专有名词/`[[实体:X]]`/颜色span；专有名词基准见 00-源文件/翻译规范.md

---

<!-- 无中文正文,以下为英文原文 -->

# Controls

  You can change your keybinds at any time here:
  

  ## Interface
  At the top left you'll see all the **menu buttons** with their corresponding hotkeys.
  Take a look at what they do, especially the emotes menu.
  Notably, the <span style="color:red">Admin Help</span> (*ahelp*) menu button will become <span style="color:red">**red**</span> if an admin is trying to contact you.

  ### Action bar
  Below the menu buttons, there's the **action bar** that shows buttons for generic and equipment-dependent <span style="color:cyan">actions</span> your character can perform.
  Hover over them to learn their function.

  It's also a **hotbar** — perform those actions by pressing their corresponding <span style="color:yellow">**number keys**</span> on your keyboard.
  Rearrange them by **dragging** one icon over another, or remove icons temporarily by dragging them away.

  ### Status bar
  Below the chat window on the right, there's the **status bar** showing your character's statuses.
  As with the action bar, hover over those icons to see what they mean.

  Some of those icons can also be clicked.
  For example, if your character ever <span style="color:orangered">catches on fire</span>, a fire icon will appear.
  You would click <span style="color:yellow">**[keybind="Use"]**</span> on it to <span style="color:cyan">drop and roll</span>.
  The same applies to <span style="color:cyan">breaking handcuffs</span> if you need to escape restraint.

  ### Inventory bar
  Along the bottom you’ll find the **inventory bar** that contains all the icons related to your equipment and storage, left to right:
  - <span style="color:cyan">clothing inventory</span> (bottom left corner) — opened with <span style="color:yellow">**[keybind="OpenInventoryMenu"]**</span> — has slots for eyes, head, neck, face, ears, body, external, hands, and shoes,
  - **PDA** slot — used to store a usable PDA that holds an ID and a pen,
  - **belt** slot — used for toolbelts and jetpacks,
  - **back** slot — normally used for satchels, backpacks and duffel bags, but it can also store medium to large weapons, and full-sized air tanks.
  - **hand** slots — you can think of them as transfer slots,
  - **pocket** slots — useful for storing small items for easy access,
  - **suit storage** slot — usable only when wearing a space suit, hardsuit or armor.
  Meant for air tanks and jetpacks, but can also hold guns.

  *Note: non-humanoid species may have slightly different slots.*

  ## Movement
  To move your character around, use <span style="color:yellow">**[keybind="MoveUp"][keybind="MoveLeft"][keybind="MoveDown"][keybind="MoveRight"]**</span>.

  Carried objects and afflictions influence your movement speed, but you can also hold <span style="color:yellow">**[keybind="Walk"]**</span> to <span style="color:cyan">walk</span>.
  This reduces your speed and helps you avoid <span style="color:cyan">slipping</span> and falling over when walking over slippery hazards like banana peels or spills.
  \n*Note: walking can be switched to a [bolditalic]toggle[/bolditalic] in the controls menu.*

  ### Spacewalks
  If you find yourself in <span style="color:#EB2D3A">zero gravity</span>, you'll still be able to move — although with reduced friction — as long as you're within reach of any structure.

  If you drift completely off station and into <span style="color:#EB2D3A">space</span>, you'll need to use the laws of motion, such as by **throwing** objects in the opposite direction.

  ## Hands
  Your character’s hands are represented by **hand slots**, which are centered along the bottom of the screen.
  - One of your hands is always the <span style="color:cyan">active hand</span>.
  - <span style="color:cyan">Swap</span> hands with <span style="color:yellow">**[keybind="SwapHands"]**</span> to control which one is active.
  - <span style="color:cyan">Take</span> items into your active, empty hand with <span style="color:yellow">**[keybind="Use"]**</span>.
  - Use <span style="color:yellow">**[keybind="Use"]**</span> to <span style="color:cyan">put</span> a held item from your active hand somewhere else, or to <span style="color:cyan">use it</span> on something or someone, depending on the context.
  - Pay attention to your active hand when interacting with the world to prevent accidentally using held items.

  **Items cannot be transferred by drag and drop.**

  ### Dropping and throwing
  Use <span style="color:yellow">**[keybind="Drop"]**</span> to <span style="color:cyan">drop</span> (or place) an item from your hand within arm's reach.
  \n<span style="color:cyan">Throw</span> items to your cursor with <span style="color:yellow">**[keybind="ThrowItemInHand"]**</span>.

  ### Pulling and pushing
  You can pull movable **entities** — items, objects, and mobs such as players, as long as you have an empty hand.
  - Use <span style="color:yellow">**[keybind="TryPullObject"]**</span> to start <span style="color:cyan">pulling</span>.
  - <span style="color:cyan">Push</span> pulled entities to your cursor with <span style="color:yellow">**[keybind="MovePulledObject"]**</span>.
  - To <span style="color:cyan">release</span>, press <span style="color:yellow">**[keybind="ReleasePulledObject"]**</span> or pull the same entity again.

  You can also use <span style="color:yellow">**[keybind="Drop"]**</span> to release pulled entities from your active hand.

  ## Interactions
  The game features **six** types of context-sensitive interactions, accessible through different methods.

  ### Standard and alternative
  Clicking <span style="color:yellow">**[keybind="Use"]**</span> performs <span style="color:cyan">standard interactions</span>.
  They heavily depend on the item you're holding and what you click on.

  Standard interactions range from clicking **tables** to put held items onto them, to **using** objects in the world with empty hands, and most commonly, using held items to interact with mobs and with other items.

  In some situations, you can directly <span style="color:cyan">swap items</span> by clicking on a machine while holding an item.
  For example, while holding a beaker, click on a machine storing another beaker. This also works with air tanks and canisters.

  Some items have <span style="color:cyan">alternative interactions</span> — use <span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span> to **lock** lockers, **eject** subitems such as batteries from other items, etc.

  ### Activation
  Interact with objects such as containers even when your hands are full by performing <span style="color:cyan">activation interactions</span> with <span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span>.
  This allows you to, for example, **open containers** without picking them up, **open doors** without using the item you're holding, and to **cycle guns**.

  Notably, press <span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span> on a mob to open the <span style="color:cyan">strip menu</span>, allowing you to view their inventory — which lets you try to take off or steal items from them.

  ### In-hand
  Many items also have <span style="color:cyan">use-in-hand interactions</span>, such as **opening** bottles, **wielding** two-handed guns and big melee weapons with both hands (clubs, spears, axes, mops, shotguns, etc.), **cycling** guns, or **toggling** syringes between injecting and drawing.

  You may just perform in-hand interactions by clicking <span style="color:yellow">**[keybind="Use"]**</span> or <span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span> on your active hand, but it's worth remembering the hotkeys — <span style="color:yellow">**[keybind="ActivateItemInHand"]**</span> and <span style="color:yellow">**[keybind="AltActivateItemInHand"]**</span> for <span style="color:cyan">standard</span> and <span style="color:cyan">alternative</span> in-hand interactions, respectively.

  ### Click and drag
  You can "use" an entity on another entity by dragging one onto another with <span style="color:yellow">**[keybind="Use"]**</span>. (Not to be confused with *pulling*.)

  Use it to:
  - <span style="color:cyan">Place</span> or force a mob (player or NPC) on a chair, bed, into a cryogenic chamber, disposal unit, etc.

  - <span style="color:cyan">Climb</span> yourself onto a table — you can also click <span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span> on the table.

  - Open the <span style="color:cyan">strip menu</span> by dragging another mob onto your character — which is also doable with <span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span>, as mentioned earlier.

  - <span style="color:cyan">Pour</span> the contents of a liquid container (janitorial trolley, bucket, beaker) into another container, a drain, a machine, etc. But first, remember to place the container on the ground — you can't do it from your inventory.

  ### Pointing
  Use <span style="color:yellow">**[keybind="Point"]**</span> to <span style="color:cyan">point</span> at a location in the world, creating a temporary arrow visible to everyone.

  ### Conclusion
  The main interactions are:
  - [bolditalic]standard[/bolditalic] (<span style="color:yellow">**[keybind="Use"]**</span>),
  - *alternative* (<span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span>),
  - **activation** (<span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span>),
  - [bolditalic]use-in-hand[/bolditalic] (<span style="color:yellow">**[keybind="ActivateItemInHand"]**</span>),
  - *alternative use-in-hand* (<span style="color:yellow">**[keybind="AltActivateItemInHand"]**</span>),
  - click and drag.

  Don't worry about having to memorize them — they're usually intuitive and consistent across entity categories, and you'll find that most entities only use one or two interactions.

  **Items stored in containers are still interactable.**

  ## Context menus
  Click <span style="color:yellow">**[keybind="UIRightClick"/]**</span> on any interactive entity to open the <span style="color:cyan">context menu</span>, which shows you additional interaction you can currently perform.
  The context menu can offer interactions such as:
  - **transferring all contents** from a container held in your active hand to another container,
  - **splitting item stacks** using presets,
  - choosing more precise **transfer amounts** for chemicals,
  - showing **deconstruction steps** for objects.

  If you click <span style="color:yellow">**[keybind="UIRightClick"/]**</span> on a pile of items, you'll open the <span style="color:cyan">entity menu</span>, listing overlapping entities you can interact with normally.

  ### Examining
  If you're ever unsure about any entity, whether it's an object or a mob, <span style="color:cyan">examine</span> it with <span style="color:yellow">**[keybind="ExamineEntity"]**</span>.
  You can also examine items listed in the entity menu.

  Besides viewing the entity's description, you'll see some icons in the bottom right of the menu:
  - a question mark icon that links to the appropriate guidebook section,
  - a lightning icon to view the item's statistics,
  - a heart icon to view a mob's health,
  - and more.

  ## Inventory and clothing
  All items can be equipped/unequipped by using <span style="color:yellow">**[keybind="Use"]**</span> on the appropriate slot.

  The easiest way to <span style="color:cyan">wear</span> (or equip) a piece of clothing is to <span style="color:cyan">use</span> it in your active hand with <span style="color:yellow">**[keybind="ActivateItemInHand"]**</span>.
  Some items don't support this, so you may need to <span style="color:cyan">manually equip them</span> them in the appropriate slot.

  **Some clothes have internal inventories and behave like containers.**

  ### Item stacks
  To <span style="color:cyan">halve</span> a stack of items, use <span style="color:yellow">**[keybind="AltActivateItemInWorld"]**</span>.

  ### Back and belt slots
  If you have a bag or a belt, open their inventories with <span style="color:yellow">**[keybind="ActivateItemInWorld"]**</span> or by clicking the mini-icons in the **bottom right** of their icons.
  You can also use the <span style="color:yellow">**[keybind="OpenBackpack"]**</span> and <span style="color:yellow">**[keybind="OpenBelt"]**</span> hotkeys for that.

  ### Smart-equipping
  You can <span style="color:cyan">quick-move</span> items between your active hand and a corresponding slot. If that slot has a container in it, this action will <span style="color:cyan">quick-store</span> or <span style="color:cyan">quick-take</span> the most recent item from that container (signified with a golden star icon in the container).

  - <span style="color:yellow">**[keybind="SmartEquipBackpack"]**</span> smart-equips the back slot.
  - <span style="color:yellow">**[keybind="SmartEquipBelt"]**</span> smart-equips the belt slot.
  - <span style="color:yellow">**[keybind="SmartEquipPocket1"]**</span>, <span style="color:yellow">**[keybind="SmartEquipPocket2"]**</span>, and <span style="color:yellow">**[keybind="SmartEquipSuitStorage"]**</span> smart-equip the left pocket, right pocket, and suit storage slots, respectively.

  ### Organizing grid inventories
  <span style="color:cyan">Rearrange</span> items by dragging them with <span style="color:yellow">**[keybind="MoveStoredItem"]**</span>.
  While dragging, <span style="color:cyan">rotate</span> them with <span style="color:yellow">**[keybind="RotateStoredItem"]**</span>.

  Click <span style="color:yellow">**[keybind="SaveItemLocation"]**</span> on an item inside a container to <span style="color:cyan">save</span> its position, so it always goes back to that position when stored.
  View saved positions by <span style="color:yellow">**hovering**</span> over items.

  ## Camera
  <span style="color:cyan">Zoom</span> the camera with <span style="color:yellow">**[keybind="ZoomIn"]**</span> and <span style="color:yellow">**[keybind="ZoomOut"]**</span> and reset with <span style="color:yellow">**[keybind="ResetZoom"]**</span>.
  \n<span style="color:cyan">Rotate</span> it with <span style="color:yellow">**[keybind="CameraRotateLeft"]**</span> and <span style="color:yellow">**[keybind="CameraRotateRight"]**</span> and reset with <span style="color:yellow">**[keybind="CameraReset"]**</span>.
  \n*Note: maps are generally designed to be played with the default camera rotation.*

  For more details about controls, you can refer to the <span style="color:cyan">Wiki</span>.
