---
title: Responsive Type
date: 2020-12-16
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: Shamama
---

![](https://forum.obsidian.md/uploads/default/optimized/2X/c/c4dc735907db26f6745fc3435e70de42405af4ed_2_690x387.png)

```css
:root
{
--font-size-normal: clamp(12px, 5vh, 20px);
--font-size-code: clamp(12px, 5vh, 18px);
--font-size-side-dock: clamp(12px, 5vh, 16px);
--font-size-side-dock-title: clamp(12px, 5vh, 18px);
--font-size-blockquote: clamp(16px, 5vh, 22px);
--font-size-status-bar: clamp(16px, 5vh, 16px);
--font-small: clamp(16px, 5vh, 18px);
--font-medium: clamp(16px, 5vh, 21px);
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/258)