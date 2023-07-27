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

**Note**: Currently, Ore Processor does not support HEX Color and placeholders. This will be implemented in future updates!\
\
To view full item configuration, use /ore docs to generate offline config documentation and select the ItemBuilder page.
