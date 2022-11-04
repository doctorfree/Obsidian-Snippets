# custom-icons-differing-files-and-folders

```css
/* get more snippets at https://github.com/kmaasrud/awesome-obsidian */
/* author: https://github.com/deathau */
/* source: https://discord.com/channels/686053708261228577/702656734631821413/755293685046050896 */

/* Emoji */
/*.nav-file-title-content::before { content: '🗒 '; }
.nav-folder-title-content::before { content: '📂 '; }*/

/* Flat font */
/* Requires: https://icomoon.io/#icons-icomoon/liga-font */
.nav-folder-children .nav-file-title-content:first-child::before {
  content: "924  ";
  font-family: "IcoMoon-Free";
}
.nav-folder-children .nav-folder-title-content::before {
  content: "930  ";
  font-family: "IcoMoon-Free";
}
```

