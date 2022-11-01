# Graph view skin

```css
/* 

This is an Obsidian Snippet to apply a skin to the Graph View

-------------------------------------------------------------

Graph View
      Circle When Not Hover
      Circle When Hover
      Line When Hover
      Circle Stroke
      Circle When Link Unresolved
      Tags
      Arrows

-------------------------------------------------------------

*/

/***************************************/
/*             Graph View              */
/***************************************/
/* Circle Stroke */
/* Line When Hover */
.graph-view.color-circle,
.graph-view.color-line-highlight {
  color: #81FFEA;
  border: 0;
}
/* Circle When Hover */
.graph-view.color-fill-highlight {
  color: #8AFF7F;
}
.graph-view.color-text {
  color: #FEFF7F;
}
.graph-view.color-line {
  color: #6272a4;
}
/* Circle When Not Hover */
.graph-view.color-fill {
  color: #81FFEA;
}
/* Arrows */
.theme-light .graph-view.color-arrow,
.theme-dark .graph-view.color-arrow {
  color: #50fa7b;
}
/* Tags */
.theme-light .graph-view.color-fill-tag,
.theme-dark .graph-view.color-fill-tag {
  color: #ffb86c;
}
/* Attachments */
.theme-light .graph-view.color-fill-attachment,
.theme-dark .graph-view.color-fill-attachment {
  color: #ff5555;
}
/* Circle When Link Unresolved */
.theme-light .graph-view.color-fill-unresolved,
.theme-dark .graph-view.color-fill-unresolved {
  color: #6272a4;
}
.workspace-leaf-content[data-type=graph] .view-content {
  background-color: hsl(207deg, 95%, 5%);
}
```
