# 📦 Main Configuration

## Ores

{% content-ref url="add-a-new-ore.md" %}
[add-a-new-ore.md](add-a-new-ore.md)
{% endcontent-ref %}

## Behaviour settings

drop-on-full-storage: Enable this option to drop items from blocks when the storage is full. Otherwise, the plugin will show a warning to the player and prevent breaking.

enable-mining-stat-on-full-storage: Enable this option to increase mining stat when storage is full. **This should only be enabled if drop-on-full-storage is set to true. Otherwise, the player can increase this stat infinitely.**

disable-offline-processing: Turn off ore processing when the player goes away. Be fine to turn this on since offline processing does not affect performance at all.

## Accessibility settings

quick-sell-ratio: Define controls for quick-sell button (Ratio)

take-amount: Define controls for taking action (Fixed amount)

craft-amount: Define controls for quick-craft button (Fixed amount)\
\
For a list of click types: [https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/ClickType.html](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/inventory/ClickType.html)

## Other settings

shop-provider: Define the shop plugin for quick-sell feature.\
Available options: ShopGUIPlus, EconomyShopGUI, EconomyShopGUI-Premium\
If you do not use quick-sell feature, simply select any option above. The plugin will automatically detect unavailable integration and disable relevant features.\
\
processing-interval: Define the processing rate in ticks\
For example, processing-interval = 5 means for every 5 ticks, try to process ores for all online players.\
\
debug-level: Will print out debug messages to the console. A higher debug level contains messages from lower levels.\
Available levels: 0, 1, 2
