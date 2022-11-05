---
title: Tag Pills
date: 2020-06-17

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: ph_
---

Insert your tag in place of `#obsidian`, `#important`, etc. to set the color specific to a tag.

![](https://forum.obsidian.md/uploads/default/original/2X/3/35df313dfde8fdbae555d251831bbc4ae8b51016.png)

```css
tag {
  background-color: var(--text-accent);
  border: none;
  color: white;
  font-size: 11px;
  padding: 1px 8px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 0px 0px;
  cursor: pointer;
  border-radius: 14px;
}
.tag:hover {
color: white;
background-color: var(--text-accent-hover);
}
.tag[href^="#obsidian"] {
  background-color: #4d3ca6;
}
.tag[href^="#important"] {
  background-color: red;
}
.tag[href^="#complete"] {
  background-color: green;
}
.tag[href^="#inprogress"] {
  background-color: orange;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/13)