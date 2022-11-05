---
title: Vim Mode Line Focus
date: 2020-06-18

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: MooddooM
---

![](https://forum.obsidian.md/uploads/default/original/2X/7/7f61432e9579a1d9086d1caad3aabfd05c1f0abf.gif)

```css
/* Cursor color in normal vim mode and opacity */
.cm-fat-cursor .CodeMirror-cursor, .cm-animate-fat-cursor {
  width: 0.5em;
  background: #d65d0e;
  opacity: 60% !important;
}

/*an active line highlight in vim normal mode */
.cm-fat-cursor .CodeMirror-activeline .CodeMirror-linebackground{
  background-color: rgba(89, 75, 95, 0.99) !important;
}

/*if you want the highlight to present in both normal and insert mode of vim*/
.CodeMirror-activeline .CodeMirror-linebackground{
  background-color: rgba(89, 75, 95, 0.99) !important;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/17)