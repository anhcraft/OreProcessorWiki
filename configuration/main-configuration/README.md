# 📦 Main Configuration

## Ores

{% content-ref url="add-a-new-ore.md" %}
[add-a-new-ore.md](add-a-new-ore.md)
{% endcontent-ref %}

<pre><code><strong>name: "Iron"
</strong>icon: iron_ingot
blocks:
  - iron_ore
  - deepslate_iron_ore
allowed-products:
  - netherite_block
</code></pre>

blocks: define a list of whitelisted blocks. A block can only be a specific ore.

allowed-products: whitelist additional items to the storage. By default, only products mentioned in the transform part are allowed. This option is recommended if you are going to use quick-craft feature.

## Behaviour settings

drop-on-full-storage: Enable this option to drop items from blocks when the storage is full. Otherwise, the plugin will show a warning to the player and prevent breaking.

enable-mining-stat-on-full-storage: Enable this option to increase mining stat when storage is full. **This should only be enabled if drop-on-full-storage is set to true. Otherwise, the player can increase this stat infinitely.**

disable-offline-processing: Turn off ore processing when the player goes away. Be fine to turn this on since offline processing does not affect performance at all.

process-silk-touch-items: By default, the plugin ignores silk-touch items. If you want it to check and process them, set to true.

## Accessibility settings

quick-sell-ratio: Define controls for quick-sell button (Ratio)

take-amount: Define controls for taking action (Fixed amount)

craft-amount: Define controls for quick-craft button (Fixed amount)\
\
For a list of click types: [https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/ClickType.html](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/ClickType.html)

## Purge settings

max-player-records: Control the maximum number of player statistics records\
The plugin will record player statistics and group them per hour\
If the records exceed the limit, the plugin will remove older ones.\
This removal does not affect all-time cumulative statistics.

max-server-records: Control the maximum number of server statistics records\
Works the same as max-player-records

## Other settings

shop-provider: Define the shop plugin for quick-sell feature.\
Available options: ShopGUIPlus, EconomyShopGUI, EconomyShopGUI-Premium\
If you do not use quick-sell feature, simply select any option above. The plugin will automatically detect unavailable integration and disable relevant features.

whitelist-worlds: Defines a list of worlds where ores will be transformed by Ore Processor.\
If you leave it empty, it implies all worlds are whitelisted.\
This feature can help improve server performance by specifying one or two worlds that the plugin will process and not all.\
\
processing-interval: Define the processing rate in ticks\
For example, processing-interval = 5 means for every 5 ticks, try to process ores for all online players.\
\
debug-level: Will print out debug messages to the console. A higher debug level contains messages from lower levels.\
Available levels: 0, 1, 2
