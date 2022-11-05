---
title: Bigger Popup Preview
date: 2020-08-07
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: _ph
---

![](https://forum.obsidian.md/uploads/default/optimized/2X/a/ac341460fac4f2ad5f1a9c823dec78e68954cf05_2_243x299.png)
![](https://forum.obsidian.md/uploads/default/optimized/2X/0/04055fe997efda1e66868a45930a8fce5b992169_2_243x299.png)

```css
/*============bigger link popup preview  ================*/
.popover.hover-popover {
    transform: scale(0.8); /* makes the content smaller */
    max-height: 800px;    /* was 300 */
    min-height: 100px;
    width: 500px;     /* was 400 */
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/82)