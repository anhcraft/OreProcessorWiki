# 📌 GUI Configuration

Ore Processor uses a component-based GUI. You define the layout made from characters. Each character defines a specific component.

The component has a type option for the plugin to handle. You can add additional items to the menu with no type.

```
title: "&0Ore Processor | Menu"
layout:
  - "---------"
  - "--XXXXX--"
  - "--XXXXX--"
  - "--XXXXX--"
  - "---------"
components:
  "-":
    name: "&e"
    material: gray_stained_glass_pane
  "X":
    type: ore
    name: "&e"
    material: black_stained_glass_pane
```

\
**Example item configuration:**

```
material: EGG # Bukkit names (case-insensitive)
amount: 3 # default to 1
damage: 5 # default to 0
name: "&aName"
lore:
- "Hello!"
enchantments:
  durability: 1 # you can use Minecraft names or Bukkit names (case-insensitive)
flags:
- hide_enchants # Bukkit names (case-insensitive)
customModelData: 1 # Set to 0 to unset custom model data
unbreakable: true
```

Material list: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html)\
Enchantment list: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/enchantments/Enchantment.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/enchantments/Enchantment.html)\
Item flags: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/ItemFlag.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/ItemFlag.html)

**Example skull configuration:**

```
material: player_head
metaType: skull
skullOwner: "notch"
skullTexture: "http://textures.minecraft.net/texture/ab8325da1f1a58e662eb1b5f58b0dbf6a7b99ec7c19f2e9c4284c7546829522d"
```
