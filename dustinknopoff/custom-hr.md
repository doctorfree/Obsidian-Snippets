---
title: Custom Symbolic HR Line
date: 2020-10-31
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: TriDiamond
---

![](https://forum.obsidian.md/uploads/default/optimized/2X/3/33b0938f405dde20178572fc09afde697b8f38f7_2_373x500.png)

```css
.markdown-preview-view hr {
  margin-block-start: 4em;
  margin-block-end: 4em;
  border: none;
  height: 1px;
  background-image: linear-gradient(to right, var(--background-primary), var(--text-accent), var(--background-primary));
}

.markdown-preview-view hr::after {
  content: '§';
  display: inline-block;
  position: absolute;
  left: 50%;
  transform: translate(-50%, -50%) rotate(60deg);
  transform-origin: 50% 50%;
  padding: 0.5rem;
  color: var(--text-sub-accent);
  background-color: var(--background-primary);
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/223)