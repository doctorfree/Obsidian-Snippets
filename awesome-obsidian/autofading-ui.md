# autofading-ui

```css
/* get more snippets at https://github.com/kmaasrud/awesome-obsidian */
/* author: https://forum.obsidian.md/u/rsdimitrov */
/* source: https://forum.obsidian.md/t/optimize-obsidian-ui-for-a-more-seamless-experience/155/5 */

/* change opacity to 0 if you want controls to fade completely */
/* auto fades note header controlls */
.view-header:not(:hover) .view-actions {
  opacity: 0.1;
  transition: opacity 0.25s ease-in-out;
}

/* auto fades status bar items */
.status-bar:not(:hover) .status-bar-item {
  opacity: 0.25;
  transition: opacity 0.25s ease-in-out;
}
```

