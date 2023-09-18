# Logging

Ore Processor has a built-in JSON logging system. Logging helps server admins to trace and analyze player behaviour such as detecting dupe, errors, etc

Currently, the plugin will track:

* Commands: add upgrade, set upgrade, add items, subtract items, store hand/all, etc
* GUI: quick-sell, store, take, quick-craft, upgrade

Maximum size per log file is 10MB. Currently, the plugin does not automatically remove old logs, so you have to keep track of this by yourself. It is recommended to retain log files in the last 1 month.
