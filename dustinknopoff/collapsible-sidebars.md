---
title: Collapsible Sidebars
date: 2020-06-16

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: cmc2397
---

```css
.workspace-ribbon.is-collapsed:not(:hover) .workspace-ribbon-collapse-btn, 
.workspace-ribbon.is-collapsed:not(:hover) .side-dock-actions, 
.workspace-ribbon.is-collapsed:not(:hover) .side-dock-settings {display:none;}
.workspace-ribbon.is-collapsed:not(:hover) {width: 0;}
.workspace-split.mod-left-split[style="width: 0px;"] {margin-left: 0;}
.workspace-split.mod-right-split[style="width: 0px;"] {margin-right: 0;}
.workspace-ribbon {transition: none}
```

Thanks to @mrjackphil and @MooddooM

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/3)