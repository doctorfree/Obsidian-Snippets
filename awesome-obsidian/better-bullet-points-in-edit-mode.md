# better-bullet-points-in-edit-mode

```css
/* get more snippets at https://github.com/kmaasrud/awesome-obsidian */
/* author: https://forum.obsidian.md/u/Piotr & https://github.com/konhi */
/* source: https://forum.obsidian.md/t/clutter-free-edit-mode/6791/30 */

div:not(.CodeMirror-activeline) > .CodeMirror-line span.cm-formatting-list-ul {
  color: transparent;
  position: relative;
}

div:not(.CodeMirror-activeline)
  > .CodeMirror-line
  span.cm-formatting-list-ul:after {
  content: "•";
  position: absolute;
  top: -6px;
  left: -1px;
  color: var(--text-normal);
  font-family: sans-serif;
  font-size: 20px;
}
```

