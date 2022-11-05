---
title: Auto fade controls
date: 2020-06-17

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: rsdimitrov
---

## Auto fade note controls

```css
.view-header:not(:hover) .view-actions {
  opacity: 0.1;
  transition: opacity .25s ease-in-out;
}
```

## Auto fade status bar

```css
/* auto fades status bar items */
.status-bar:not(:hover) .status-bar-item {
  opacity: 0.25;
  transition: opacity .25s ease-in-out;
}
```

## Subtler scrollbars

```css
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, ::-webkit-scrollbar {
  width: 3px;
  height: 3px;
}
```

## Subtler folding arrows

```css
/* Make subtler folding gutter arrows */
.CodeMirror-foldgutter-folded:after, .CodeMirror-foldgutter-open:after {
    opacity: 0.5;
    font-size: 60%;
}

.CodeMirror-foldgutter-folded:hover:after, .CodeMirror-foldgutter-open:hover:after {
    opacity: 1;
}

.CodeMirror-foldgutter-folded:after {
    content: "\25BA";    
}

.CodeMirror-foldgutter-open:after {
    content: "\25BC";    
}

```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/10)