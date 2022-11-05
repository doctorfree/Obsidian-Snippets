---
title: Changing Font Styles/Sizes
date: 2020-12-06
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: argentum
---

```css
 /*----------------------------------------------------------------
  Font styles
  Preview mode and UI */

  --text:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
  
  /* Editor mode */

  --text-editor:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen-Sans,Ubuntu,Cantarell,"Helvetica Neue",sans-serif;
  
  /* Code */

  --font-monospace:Menlo,SFMono-Regular,Consolas,"Roboto Mono",monospace;

  /* Sizes, weights, padding */

  --font-normal:16px;
  --font-small:13px;
  --font-smaller:11px;
  --font-smallest:10px;
  --normal-weight:400;   /* Switch to 300 if you want thinner default text */
  --bold-weight:600;     /* Switch to 700 if you want thicker bold text */
  --line-width:40rem;    /* Maximum characters per line */
  --line-height:1.5;
  --max-width:87%;       /* Amount of padding around the text, use 90% for narrower padding */
  --nested-padding:3.5%; /* Amount of padding for quotes and transclusions */
  --icon-muted:0.4;
  --border-width:1px;
  --border-width-alt:1px;

  /*----------------------------------------------------------------
```

[Original Snippet](https://github.com/kepano/obsidian-minimal/blob/master/obsidian.css#L116)

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/248)