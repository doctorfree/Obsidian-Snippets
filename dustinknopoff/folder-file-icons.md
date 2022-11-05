---
title: Folder and File Icons in Explorer
date: 2020-09-15
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: deathau
---

```css
.nav-folder-children .nav-file-title-content:first-child::before { content: '🗒 '; }
.nav-folder-children .nav-folder-title-content::before { content: '📂 '; }
```

## Using Wingdings or [IcoMoon](https://icomoon.io/#icons-icomoon/liga-font)

```css
.nav-folder-children .nav-file-title-content:first-child::before {
    content: "\e924  ";
    font-family: 'IcoMoon-Free';
  }
  .nav-folder-children .nav-folder-title-content::before {
    content: '\e930  ';
    font-family: 'IcoMoon-Free';
  }
```

![](https://forum.obsidian.md/uploads/default/original/2X/7/79c75764a0400ceff97f36e518c4002b2d2a764a.png)