# typography

```css
/* TYPOGRAPHY */

.subtle {
  color: var(--h6);
  letter-spacing: 0.02em;
  font-weight: var(--h6-weight);
  font-size: var(--h6);
}

.small-caps {
  font-variant: small-caps;
}

/* Colors */

.red {
  color: var(--red)
}

.orange {
  color: var(--orange)
}

.yellow {
  color: var(--yellow)
}

.green {
  color: var(--green)
}

.cyan {
  color: var(--cyan)
}

.blue {
  color: var(--blue)
}

.purple {
  color: var(--purple)
}

.pink {
  color: var(--pink)
}


/* Strikethrough */

.cm-strikethrough, del {
    color: var(--text-faint);
    text-decoration: line-through;
    transition: color 220ms cubic-bezier(0.45,0.05,0.55,0.95);
}

.cm-strikethrough:hover, del:hover {
    text-decoration: none;
    color: var(--text-normal);
    transition: color 220ms cubic-bezier(0.45,0.05,0.55,0.95);
}

/*~ Ordered List / Number List ~*/

ol > li::marker,
.cm-s-obsidian span.cm-formatting-list {
    font-weight: var(--font-regular);
    font-size: var(--font-scale-0-5);
    color: var(--text-muted);
    font-family: var(--font-monospace);
}

ol {
    list-style-type: decimal;
}
ol ol {
    list-style-type: lower-alpha;
}
ol ol ol {
    list-style-type: decimal;
}
ol ol ol ol {
    list-style-type: lower-alpha;
}
ol ol ol ol ol {
    list-style-type: decimal;
}
ol ol ol ol ol ol {
    list-style-type: lower-alpha;
}
ol ol ol ol ol ol ol {
  list-style-type: decimal;
}
ol ol ol ol ol ol ol ol {
    list-style-type: lower-alpha;
}
ol ol ol ol ol ol ol ol ol {
    list-style-type: decimal;
}
ol ol ol ol ol ol ol ol ol ol {
    list-style-type: lower-alpha;
}
ol ol ol ol ol ol ol ol ol ol ol {
    list-style-type: decimal;
}
ol ol ol ol ol ol ol ol ol ol ol ol {
    list-style-type: lower-alpha;
}
ol ol ol ol ol ol ol ol ol ol ol ol ol {
    list-style-type: decimal;
}
ol ol ol ol ol ol ol ol ol ol ol ol ol ol {
    list-style-type: lower-alpha;
}
ol ol ol ol ol ol ol ol ol ol ol ol ol ol ol {
    list-style-type: decimal;
}
ol ol ol ol ol ol ol ol ol ol ol ol ol ol ol ol {
    list-style-type: lower-alpha;
}
/*~ Unordered List / Bullet List ~*/

ul {
    list-style-type: disc;
}
ul ul {
    list-style-type: circle;
}
ul ul ul {
    list-style-type: square;
}
ul ul ul ul {
    list-style-type: disc;
}
ul ul ul ul ul {
    list-style-type: circle;
}
ul ul ul ul ul ul {
    list-style-type: square;
}
ul ul ul ul ul ul ul {
    list-style-type: disc;
}
ul ul ul ul ul ul ul ul {
    list-style-type: circle;
}
ul ul ul ul ul ul ul ul ul {
    list-style-type: square;
}
ul ul ul ul ul ul ul ul ul ul {
    list-style-type: disc;
}
ul ul ul ul ul ul ul ul ul ul ul {
    list-style-type: circle;
}
ul ul ul ul ul ul ul ul ul ul ul ul {
    list-style-type: square;
}
ul ul ul ul ul ul ul ul ul ul ul ul ul {
    list-style-type: disc;
}
ul ul ul ul ul ul ul ul ul ul ul ul ul ul {
    list-style-type: circle;
}
ul ul ul ul ul ul ul ul ul ul ul ul ul ul ul {
    list-style-type: square;
}

.callout-title-inner {
    font-family: 'Century Gothic';
}
```

