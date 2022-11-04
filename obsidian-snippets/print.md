# print

```css
@media print {

  /* Setting content width, unsetting floats and margins */
  .markdown-preview-view {
    width: 100%;
    margin: 0;
    float: none;
  }

  /* Set margins */
  @page {
    margin: 1in;
  }

  /* Fonts */
  body {
    font-family: Palatino, "Palatino Linotype", "Palatino LT STD", "Book Antiqua", Georgia, serif;
    line-height: 1.3;
  }

  h1, h2, h3, h4, h5, h6 {
    font-family: "Century Gothic", CenturyGothic, AppleGothic, sans-serif;
  }

  th {
    font-weight: bold !important;
  }

  /* Colors */
  body, th, em, strong, del, h1, h2, h3, h4, h5, pre, code, .token,
  .markdown-preview-view ul>li.task-list-item.is-checked,
  ol>li::marker, ul>li::marker, blockquote, .admonition {
    background: white !important;
    color: black !important;
  }

  .admonition {
    border-left: none !important;
    box-shadow: none !important;
  }

  .admonition-title-icon {
    color: gray !important;
  }

  del {
    color: slategray !important;
  }

  h6 {
    background: white !important;
    color: darkslategray !important;
  }

  hr {
    border-color:gray !important;
  }

/* Tables */

  table, thead, th, tbody, td {
    border: none !important;
  }

  tr {
    border-bottom: lightgray dotted 1px;
    color: black !important;
  }

  tr:nth-child(odd){
    background: white;
  }

  tr:nth-child(even){
    background: gainsboro;
  }

  /* Page Breaks */
  a {
    page-break-inside:avoid;
  }

  blockquote, .admonition {
    page-break-inside: avoid;
  }

  h1, h2, h3, h4, h5, h6 {
    page-break-after:avoid;
    page-break-inside:avoid;
  }

  img {
    page-break-inside:avoid;
    page-break-after:avoid;
  }

  table, pre {
    page-break-inside:avoid;
  }

  ul, ol, dl, div.math-block {
    page-break-before:avoid;
  }

  /* Displaying link color and link behaviour */
  a:link, a:visited, a {
    background: transparent;
    color: black;
    text-decoration: underline;
    text-align: left;
  }

  a[href^=http]:after {
    content:" < " attr(href) "> ";
  }

  a:after > img {
    content: "";
  }

  article a[href^="#"]:after {
    content: "";
  }

  a.external-link::after {
    content:" <" attr(href) "> ";
    font-style:italic;
    font-size: 0.9em;
  }

  /**
  * Making intergated videos disappear, and removing the iframes' whitespace to zero.
  */

  .entry iframe, ins {
      display: none;
      width: 0 !important;
      height: 0 !important;
      overflow: hidden !important;
      line-height: 0pt !important;
      white-space: nowrap;
    }

  .embed-youtube, .embed-responsive {
    position: absolute;
    height: 0;
    overflow: hidden;
  }

  /* Hide unnecessary Elements */

  body.minimal-rel-preview:not(.ig-lists-preview) .markdown-preview-view ul ul,
  body.minimal-rel-preview:not(.ig-lists-preview) .markdown-preview-view ol ul,
  body.minimal-rel-preview:not(.ig-lists-preview) .markdown-preview-view ul ol,
  body.minimal-rel-preview:not(.ig-lists-preview) .markdown-preview-view ol ol {
    border: none;
  }

  .task-list-item a[href="#task"] {
    display: none;
  }

  /* Hide scrollbars */
  ::-webkit-scrollbar {
    display:none;
  }

  /* Type Rhythm */
  p + p {
    text-indent: 1em;
  }

  p {
      margin: 0 auto;
  }

  dl + p, ol + p, ul + p, div.math-block {
      margin-top: 2.8rem;
  }

}
```

