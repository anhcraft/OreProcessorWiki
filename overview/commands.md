# Commands

/ore: open main menu\
/ore inspect \<player>: inspect primary data of an online/offline player\
/ore reload: reload the plugin\
/ore docs: generate offline documentation\
\
/ore store hand: Store the item in hand in a suitable ore storage\
/ore store all: Store all appropriate items in the inventory to suitable ore storage

/ore upgrade throughput set \<player> \<ore> \<amount>\
/ore upgrade throughput add \<player> \<ore> \<amount>\
/ore upgrade capacity set \<player> \<ore> \<amount>\
/ore upgrade capacity add  \<player> \<ore> \<amount>\
_To upgrade all ore, set \<ore> to \*_\
_The commands support offline player_\
\
/ore add \<player> \<ore> \<material> \<amount> \[\<force: true/false>]: add item to an ore storage \
/ore subtract \<player> \<ore> \<material> \<amount>: take item from an ore storage\
/ore set \<player> \<ore> \<material> \<amount> \[\<force: true/false>]: put item into an ore storage \
_The commands support offline player_\
\
/ore stats server \<ore query>: view server statistics\
/ore stats player \<player> \<ore query>: view player statistics\
_To select multiple ores, use commas, e.g: `iron,gold,diamond`_\
_To select all ores, use \*_\
_The commands support offline player_
