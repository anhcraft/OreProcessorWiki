# Logging

Ore Processor has a built-in JSON logging system. Logging helps server admins to trace and analyze player behaviour such as detecting dupe, errors, etc

Currently, the plugin will track:

* Commands: add upgrade, set upgrade, add items, substract items, store hand/all, etc
* GUI: quick-sell, store, take, quick-craft, upgrade

Maximum size per log file is 10MB. Currently the plugin does not remove old logs automatically so you have to keep track this by yourself.&#x20;

It is recommended to retain log files in the last 1 month to prevent any unexpected situations from happening.
