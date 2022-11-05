---
title: Collapsible Side Notes
date: 2021-03-04
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: cmjn
---

![](https://forum.obsidian.md/uploads/default/optimized/2X/a/a64f3a0c95b262030c88ad5e82cabee7130f5884_2_690x237.jpeg)

```css
blockquote {
    border: none !important;
    padding: 0 20px;
}

blockquote .task-list-item {
    font-family: var(--font-stack-ui) !important;
    font-size: var(--font-size-secondary) !important;
    line-height: 1.35em;
    font-style: normal;
    position: absolute;
    text-align: justify;
    z-index: 1;
    color: var(--text-faint) !important;
    right: min(calc(50% + 0.5 * var(--line-width) + 2.5em), calc(100% - 3.5em));
    width: calc(50% - 0.5 * var(--line-width) - 3em);
    max-width: calc(0.66 * var(--line-width));
    min-width: 3em;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    margin-block-start: 0 !important;
    margin-block-end: 0 !important;
    text-indent: 0 !important;
}
blockquote .task-list-item > .task-list-item-checkbox {
    appearance: none;
    position: absolute;
    height: 100%;
    width: 100%;
    left: 0;
    top: 0;
    background: none !important;
    background-color: transparent !important;
    margin: 0 !important;
    border: none;
    cursor: pointer;
}
blockquote .task-list-item.is-checked {
    z-index: 999;
    color: var(--text-normal) !important;
    right: min(calc(50% + 0.5 * var(--line-width) + 2.5em), calc(100% - 12.5em));
    min-width: 12em;
    overflow: visible;
    max-height: none;
    white-space: normal;
    text-decoration: none !important;
}

```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/341)