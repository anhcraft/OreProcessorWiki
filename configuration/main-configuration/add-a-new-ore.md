# Add a new ore

## Getting started

Firstly, duplicate an existing configuration in the "ore" section.

```
ores:
  coal:
    name: "Coal"
    icon: coal
    blocks:
      - coal_ore
      - deepslate_coal_ore
    transform:
      default:
        - coal > coal
  # Below is what we just copied
  coal:
    name: "Coal"
    icon: coal
    blocks:
      - coal_ore
      - deepslate_coal_ore
    transform:
      default:
        - coal > coal
```

For example, we want to add amethyst as a new ore. We change the id, the name, the icon.\
Remember, for material names, you can look up them there: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html)\
\
Then, you have to choose which blocks will produce the ore. It is possible to mix multiple blocks which produce different drops. Because we will filter and transform the drops in the "transform" section later.

```
ores:
  // ....
  amethyst:
    name: "Amethyst"
    icon: amethyst_block
    blocks:
      - amethyst_block
    transform:
      default:
        - coal > coal # Read below to change this line
```

The most important is the "transform" section. With Ore Processor, you can define multiple transformations **requiring player permissions**. Default one is always **required**, and has **no permission** requirement.\
The "transform" list will handle from **bottom to top**. So you should always put the default first and put the most incentive last.

## Transformation syntax

Each transform group contains multiple transformations. This defines the ore processing circuit. For the basic syntax:

<pre><code><strong>default:
</strong><strong> - amethyst_block > amethyst_block
</strong></code></pre>

The first line means: When a block drops an amethyst block, turns it into an amethyst block and moves to the storage. We call the material on the left side "**feedstock**", and the right side "**product**".\
The above transform is unary (as feedstock is the same as the product). It does not change the drop at all, but that transform is required to move the block to the storage. **If it is undefined, the drop is untouched.**\
\
Assume, we want to change the block into an amethyst cluster, the syntax will be:

```
default:
 - amethyst_block > amethyst_cluster
```

You may ask how to apply chances here. For example, there is a 30% chance to receive a cluster, and a 70% chance to obtain a full block:

```
default:
 - amethyst_block > 30% amethyst_cluster, 70% amethyst_block
```

## Advanced transformation

In fact, Ore Processor uses "weight" system. The weight of each product is used to determine the chance. Percentage character (%) is **optional** and does not change the calculation.\
\
For example, amethyst\_cluster has a weight of 100, amethyst\_block has a weight of 200, and amethyst\_shard has a weight of 500.\
\
Total Weight: $$W = 100+200+500=800$$\
Chance of amethyst\_cluster: $$W_{1} = 100/800=0.125=12.5\%$$\
Chance of amethyst\_block: $$W_{2} = 200/800=0.25=25\%$$\
Chance of amethyst\_shard: $$W_{1} = 500/800=0.625=62.5\%$$\
If you sum up the chances above: $$12.5\% + 25\% + 62.5\% = 100\%$$\
\
The syntax will be:

```
default:
 - amethyst_block > 100 amethyst_cluster, 200 amethyst_block, 500 amethyst_shard
```

It is also possible to set the amount per product. If not specified, defaults to 1.\
For example, with the syntax below:

```
default:
 - amethyst_block > 10 amethyst_cluster, 20% amethyst_shard:3
```

That means the product can be either amethyst\_cluster or amethyst\_shard, where amethyst\_cluster has a weight of 10 and x3 amethyst\_shard has a weight of 20. _Remember, percentage character (%) does not matter as mentioned above._

## Put into Practice

Most servers will have some incentives for donors. Assume, we have three ranks Member, VIP and MVP. Members will use the default transformation, so we make another two transformation groups.\
\- Default: has 40% to obtain amethyst\_block\
\- VIP: has 100% to obtain amethyst\_block\
\- MVP: has 70% to obtain x2 amethyst\_block, and an additional 30% chance to obtain amethyst\_cluster

```
ores:
  // ....
  amethyst:
    name: "Amethyst"
    icon: amethyst_block
    blocks:
      - amethyst_block
    transform:
      default:
        - amethyst_block > 40% amethyst_block, 60% air
      vip:
        - amethyst_block > 100% amethyst_block
      mvp:
        - amethyst_block > 70 amethyst_block:2, 30 amethyst_cluster
```

Important note: To give 40% amethyst\_block, you have to put 60% air. The plugin will ignore air before putting it into storage. If you do not define 60% air, the plugin will think that amethyst\_block has 30 weight, and because there is no other item, it has a chance of 100%.
