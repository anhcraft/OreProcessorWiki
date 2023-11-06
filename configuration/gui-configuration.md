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

## Item Meta

```yaml
material: player_head
# Other general item settings...
meta:
  type: skull # <===========
  # Other item meta settings...
```

### Skull

```yaml
material: player_head
meta:
  type: skull
  skull-texture: "6e2be91f04579a924a20a0585b8addac8ec790c97f005333a47ed983554c6ea"
```

The skull texture is an identifier at the tail of the skin URL pointing to Mojang's server such as [https://textures.minecraft.net/texture/**6e2be91f04579a924a20a0585b8addac8ec790c97f005333a47ed983554c6ea**](https://textures.minecraft.net/texture/6e2be91f04579a924a20a0585b8addac8ec790c97f005333a47ed983554c6ea)

It is possible to use the URL. However, I won't recommend it since that is too long

### Banner

<pre class="language-yaml"><code class="lang-yaml"><strong>material: white_banner
</strong>meta:
    type: banner
    banner-patterns:
    - pattern: bricks
        color: gray
    - pattern: mojang
        color: red
</code></pre>

Pattern type: [https://hub.spigotmc.org/javadocs/spigot/org/bukkit/block/banner/PatternType.html](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/block/banner/PatternType.html)

Dye color: [https://hub.spigotmc.org/javadocs/spigot/org/bukkit/DyeColor.html](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/DyeColor.html)

### Armor

```yaml
material: diamond_chestplate
meta:
    type: armor
    trim-material: quartz
    trim-pattern: dune
```

Trim pattern: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimPattern.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimPattern.html)

Trim material: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimMaterial.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimMaterial.html)
