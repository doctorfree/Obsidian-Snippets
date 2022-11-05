---
title: Variable Embed Heights
date: 2020-06-21

taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: foreveryone
---
This snippet will make embeds sit within a text without scrollbars by default. If a link is given the alias `[[short|document]]]` or `![[tall|document]]` it will be set to a limited height and given scroll bars if it exceeds the maximum height.
```css
.markdown-preview-view .markdown-embed-content { 
  max-height: unset;
}

.internal-embed.is-loaded[alt="short"] {
  max-height: 45vh !important;
  overflow: auto !important;
  padding-right: 0px!important;
}

.internal-embed.is-loaded[alt="tall"] {
  max-height: 80vh !important;
  overflow: auto !important;
}
```
