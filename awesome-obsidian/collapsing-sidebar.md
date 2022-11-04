# collapsing-sidebar

```css
/* get more snippets at https://github.com/kmaasrud/awesome-obsidian */
/* author: https://github.com/kmaasrud */
/* source: https://github.com/kmaasrud/awesome-obsidian */

.workspace {
  position: relative;
}

.side-dock-ribbon.mod-left.is-collapsed,
.side-dock-ribbon.mod-right.is-collapsed {
  height: 100%;
}

.side-dock-ribbon.mod-left.is-collapsed:not(:hover),
.side-dock-ribbon.mod-right.is-collapsed:not(:hover) {
  position: absolute;
  opacity: 0;
}

.side-dock-ribbon.mod-left.is-collapsed:not(:hover) {
  left: 0;
}

.side-dock-ribbon.mod-right.is-collapsed:not(:hover) {
  right: 0;
}
```

