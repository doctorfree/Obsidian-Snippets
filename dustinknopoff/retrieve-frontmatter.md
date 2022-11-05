---
title: Retrieving a File's Frontmatter
date: 2021-05-15

taxonomies:
  tags:
    - development
  kind:
    - plugins
extra:
  author: Christian
---

```js
if (file instanceof TFile) {
  this.app.metadataCache.getFileCache(file).frontmatter; // Is [key: string]: any | undefined
}
```