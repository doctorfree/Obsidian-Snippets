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

:root {
    --white: #F8F8F3;
    --gray-1: #586e75;
    --gray-2: #D5D4DE;
    --red: #FF5555;
    --orange: #FE9580;
    --green: #8AFF7F;
    --cyan: #81FFEA;
    --cyan-transparent: rgba(129, 255, 234, 0.3);
    --purple: #9580FF;
    --purple-transparent: rgba(149, 128, 255, 0.5);
    --pink: #FE7FBF;
    --blue: #00588E;
    --yellow: #FEFF7F;
}

/* Circle Stroke */
.graph-view.color-circle {
  color:var(--green) !important;
}
.graph-view.color-line-highlight {
  color:var(--cyan) !important;
  border:0 !important;
}
/* Circle When Hover */
.graph-view.color-fill-highlight {
  color:var(--yellow) !important;
}
.graph-view.color-text {
  color:var(--cyan) !important;
}
.graph-view.color-line {
  color: #6272a4 !important;
}
/* Circle When Not Hover */
.graph-view.color-fill {
    color:var(--white) !important;
}
/* Arrows */
.graph-view.color-arrow {
  color: var(--cyan) !important;
}
/* Tags */
.graph-view.color-fill-tag {
  color: var(--green) !important;
}
/* Attachments */
.graph-view.color-fill-attachment {
  color: var(--gray-1) !important;
}
/* Circle When Link Unresolved */
.graph-view.color-fill-unresolved {
  color:var(--blue) !important;
}
```