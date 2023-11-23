# FAQ

1. **What are the differences between the free and premium versions?**

Compared to the premium version, the free one does not contain the following features:

* Quick-sell
* Quick-craft
* JSON logging
* Inspect
* Upgrade commands
* Store commands
* Statistics commands

2. **Only ore materials supported?**&#x20;

You can use any block material such as cobblestone, amethyst, or even bedrock

3. **Does it work with plugin X?**&#x20;

The plugin is developed to be compatible with as many plugins as possible. However, not all of them work in a standard way and require integration. If your favourite plugin does not work with OreProcessor, please contact me!

4. **What about the cost of performance?**&#x20;

The plugin is super lightweight as it does not behave like Minecraft's ticking system. I have tested the plugin on a server with thousands of ores processed per second and the plugin is even not in the top 10 in /timings.

5. **Will upgrading to the Premium version require player-data reset?**&#x20;

There is 100% no data loss. The player data format is compatible with both Lite and Premium versions without conversion or reset.

6. **How to use RGB messages?**

You can utilize RGB in chat messages and GUI. The format is \&#aaaaaa for e.g: \&#2dbd6b

7. **I saw warnings/errors in the console!**

The plugin will validate the configuration upon startup / when you reload the plugin.

Typically, warnings are shown in yellow, and serve errors are shown in red. You need to read those messages to understand what is going on.&#x20;

For example, if you got these messages:

```
[16:29:33 WARN]: [OreProcessor] Unknown material 'raw_iron' in phase 'raw_iron > raw_iron'
[16:29:33 WARN]: [OreProcessor] Unknown material 'raw_iron' in phase 'raw_iron > iron_ingot'
[16:29:33 WARN]: [OreProcessor] Unknown material 'raw_iron' in phase 'raw_iron > 80 cobblestone, 60 iron_ingot, 10 gold_ingot, 5 diamond'
[16:29:33 WARN]: [OreProcessor] Unknown material 'raw_gold' in phase 'raw_gold > raw_gold'
[16:29:33 WARN]: [OreProcessor] Unknown material 'raw_gold' in phase 'raw_gold > gold_ingot'
[16:29:33 WARN]: [OreProcessor] Invalid material 'copper_ingot' in phase '9 copper_ingot'
[16:29:33 WARN]: [OreProcessor] Invalid crafting input in phase '9 copper_ingot > 1 copper_block'
```

That means you have configured wrong materials / or you are using materials from newer versions on a server running the older version. In this case, you can update the configuration or simply ignore the warning. Any missing material will be ignored by the plugin.

The default configuration contains materials such as amethyst or copper which exist on 1.17+, you will see those warnings on 1.16 and older servers. But again, they can be ignored!
