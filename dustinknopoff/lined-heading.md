---
title: Lined Heading
date: 2021-01-06
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: frvkl
---

![](https://forum.obsidian.md/uploads/default/optimized/2X/3/31bfb6c7a099447639685da0dfac6b5c0d2d714a_2_690x58.png)

```css
h1 {
	display: flex;
	width: 100%;
	align-items: center;
}
h1:before,
h1:after{
	content: '';
	background: gray;
	height: .1em;
	margin: .2em;
	flex: 1;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/288)