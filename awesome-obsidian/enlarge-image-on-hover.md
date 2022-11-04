# enlarge-image-on-hover

```css
/* get more snippets at https://github.com/kmaasrud/awesome-obsidian */
/* author: https://forum.obsidian.md/u/den/summary */
/* source: https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/29 */

.markdown-preview-view img {
  display: block;
  margin-top: 20pt;
  margin-bottom: 20pt;
  margin-left: auto;
  margin-right: auto;
  width: 50%; /* experiment with values */
  transition: transform 0.25s ease;
}

.markdown-preview-view img:hover {
  -webkit-transform: scale(1.8); /* experiment with values */
  transform: scale(2);
}
```

