---
title: Enlarge Image on Hover
date: 2020-06-28

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: den
---


```css
.markdown-preview-view img {
  display: block;
  margin-top: 20pt;
  margin-bottom: 20pt;
  margin-left: auto;
  margin-right: auto;
  width: 50%;  /* experiment with values */
  transition:transform 0.25s ease;
}

.markdown-preview-view img:hover {
    -webkit-transform:scale(1.8); /* experiment with values */
    transform:scale(2);
    
}

```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/29)