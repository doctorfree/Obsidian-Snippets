---
title: Bullet Point Relationship Lines
date: 2020-06-16

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: deathau
---

```css
.cm-hmd-list-indent .cm-tab, ul ul { position: relative; }
.cm-hmd-list-indent .cm-tab::before, ul ul::before {
 content:'';
 border-left: 1px solid rgba(0, 122, 255, 0.25);
 position: absolute;
}
.cm-hmd-list-indent .cm-tab::before { left: 0; top: -5px; bottom: -4px; 
}
ul ul::before { left: -11px; top: 0; bottom: 0; 
} 

```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/2)