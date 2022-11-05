# calendar-emoji

```css
#calendar-container [data-emoji-tag]::after {
  content: attr(data-emoji-tag);
  position: absolute;
  top: -4px;
  right: 4px;
  height: 8px;
  width: 8px;
}

.frontmatter-section-tags .tag[href^='#flagged'],
.frontmatter-section-tags .tag[href^='#🎂'],
.frontmatter-section-tags .tag[href^='#🦃'],
.frontmatter-section-tags .tag[href^='#🌴'] {
  display: none !important;
}
```

