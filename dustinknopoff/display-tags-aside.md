---
title: Display Tags Aside
date: 2021-02-26
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: cmjn
---

![](https://forum.obsidian.md/uploads/default/optimized/2X/d/d12f002545f09ee9486ecdaa7879912be533f9b9_2_690x98.jpeg)
![](https://forum.obsidian.md/uploads/default/optimized/2X/1/1cf2b3239a24f3b0c3176580c1d88fc0b4f43fec_2_690x97.jpeg)

```css
p > a.tag {
    font-size: 0;
    width: 0;
    padding: 0;
    margin: 0;
    background: none;
    text-decoration: none;
    border: none;
}
p > a.tag::before {
    content: '#';
    font-size: 16px;
}
p > a.tag::after {
    content: attr(href);
    float: right;
    min-width: 3ch;
    max-width: 25%;
    margin-right: calc(-25% - 1.5em);
    margin-left: calc(-25% - 1.5em);
    position: relative;
    clear: right;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
    font-size: 16px;
}

p > a.tag:hover::after {
    max-width: fit-content !important;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/327)