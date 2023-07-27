# 🚀 Upgrade Configuration

Ore Processor has a built-in upgrade system. The upgrade feature is super simple. Currently there are two upgrade types: Capacity and Throughput

* Capacity: Higher capacity allows storing more products in storage
* Throughput: Higher throughput will process ore faster

**Note**: Upgrade is per ore and per player

**An upgrade must have a default level**. Additional ones can be added with the following **rule**: The later upgrade, the higher amount is.

```
throughput-upgrade:
  default:
    amount: 1
  level-1:
    amount: 2
    cost: 50000
  level-3:
    amount: 3
    cost: 100000
  level-4:
    amount: 4
    cost: 300000
capacity-upgrade:
  default:
    amount: 128
  level-1:
    amount: 192
    cost: 30000
  level-3:
    amount: 256
    cost: 50000
  level-4:
    amount: 320
    cost: 100000
```
