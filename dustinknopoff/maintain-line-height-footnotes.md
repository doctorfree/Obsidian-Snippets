---
title: Maintain Line Height - Footnotes
date: 2021-03-04
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: phlind
---

Before:
![](https://forum.obsidian.md/uploads/default/original/2X/1/1e2c18708833addaf9abcb6dc06d6391f682eb97.png)

After:
![](https://forum.obsidian.md/uploads/default/original/2X/3/3aaff87ddbb77e93983f40bf9e120578749e961f.png)

```css
/* Stop footnotes affecting line height */
sup { 
	vertical-align: top; 
	position: relative; 
	top: -0.3em; 
	font-size: 0.75em; 
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/342)