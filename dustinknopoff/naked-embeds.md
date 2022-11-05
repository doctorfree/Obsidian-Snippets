---
title: Naked Embeds
date: 2020-06-18

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: deathau
---

Embeds the contents of linked notes into the preview

![](https://forum.obsidian.md/uploads/default/optimized/2X/d/d33d0de07d58894ab485b37c9806ff88a447fb6a_2_690x136.png)

```css
/* Naked Embeds */
.markdown-embed-title { display: none; }
.markdown-preview-view .markdown-embed-content>:first-child { margin-top: 0;}
.markdown-preview-view .markdown-embed-content>:last-child { margin-bottom: 0;}

/*remove the following two line, you will get border and scroll*/
.markdown-preview-view .markdown-embed { border:none; padding:0; margin:0; }
.markdown-preview-view .markdown-embed-content { 
  max-height: unset;
  background-color: var(--background-secondary); /*define different bg color*/
}

/* the link on the top right corner*/
.markdown-embed-link {
color: var(--text-faint) !important;
}

.markdown-embed-link:hover {
color: var(--text-accent) !important;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/19)