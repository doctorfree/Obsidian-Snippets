---
title: Stylish Blockquotes
date: 2020-07-04
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: Thery
---

## Add quotation mark before quote

![](https://forum.obsidian.md/uploads/default/original/2X/a/a64ba8a02dea06dc2fa741f167d7a18b2b52db07.png)

```css
/* Add quotation character before quote */
blockquote:before {
  font: 14px/20px italic Times, serif;
  content: "“";
  font-size: 3em;
  line-height: 0.1em;
  vertical-align: -0.4em;
}
blockquote p { display: inline; }
```

## Remove left margin

![](https://forum.obsidian.md/uploads/default/original/2X/c/ca4834dc2741c16320ec45873105c3d3804fb2a1.png)

```css
/* Remove blockquote left margin */
blockquote {
  margin-inline-start: 0;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/39)