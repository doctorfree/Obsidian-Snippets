![](assets/obsidian.png)

# Obsidian-Snippets

This repository contains various CSS snippets written for [Obsidian](https://obsidian.md).

Snippets included here have been gathered and curated by [Doctorfree](https://github.com/doctorfree) and include freely redistributable snippets from:

- [Dmytro Shulha](https://github.com/Dmytro-Shulha/obsidian-css-snippets)
- [Knut Magnus Aasrud](https://github.com/kmaasrud/awesome-obsidian/tree/master/code/css-snippets)
- [Scott Killen](https://github.com/ScottKillen/obsidian-snippets)
- [Dustin Knopoff](https://github.com/dustinknopoff/obsidian-snippets)

Some of these snippets were initially collected by [Klaas](https://forum.obsidian.md/t/how-to-achieve-css-code-snippets/8474) and further curated by [Erica](https://github.com/ericaxu).

## Table of Contents

- [Usage](#usage)
    - [Obsidian](#obsidian)
    - [Markdown viewers](#markdown_viewers)
    - [Clone and view locally](#clone_and_view_locally)
- [Included snippets](#included_snippets)
    - [Dmytro-Shulha](#dmytro-shulha)
    - [Knut Magnus Aasrud](#awesome_obsidian)
    - [ScottKillen](#scottkillen)
    - [DustinKnopoff](#dustinknopoff)
- [Support](#support)

## Usage

The Obsidian CSS snippets in this repository are embedded as code blocks in markdown for ease of viewing. To create a CSS snippet use the `Copy` button in the upper right hand corner of the CSS code block when viewing the markdown in Obsidian. This will copy the CSS snippet to the clipboard. Paste the contents of the clipboard into a file, typically named the same as the markdown but with a `.css` filename extension rather than `.md`. Alternatively, copy the markdown file to a new file with `.css` extension rather than `.md` and delete ``all lines up to and including the line beginning with ```css`` and ``all lines after and including the line beginning with ```.``

To use an Obsidian CSS snippet in an Obsidian vault, copy the snippet to the folder `/path/to/vault/.obsidian/snippets/`. For example, to use a snippet named `MySnippet.css` in an Obsidian vault located at `/home/ronnie/Documents/MyVault/`:

```shell
mkdir -p /home/ronnie/Documents/MyVault/.obsidian/snippets
cp /path/to/MySnippet.css /home/ronnie/Documents/MyVault/.obsidian/snippets`
```

After the snippet is placed in the Obsidian `snippets` folder, enable it in Obsidian by opening the `MyVault` vault in Obsidian and navigating to `Settings -> Appearance -> CSS snippets`. The `MySnippet` CSS snippet should show up there as a disabled snippet. Click the slider toggle to the right of the snippet to enable it. The `MySnippet` CSS styling will immediately be applied to your vault documents.

### Obsidian

Any [markdown](https://en.wikipedia.org/wiki/Markdown) viewer can be used to view this knowledge base. You can simply browse the repository and click on the individual markdown files at https://github.com/doctorfree/Obsidian-Snippets.git in any web browser. However, to view the inter-relationships between the many components, categories, and technologies documented here, we recommend using the [Obsidian](https://obsidian.md) knowledge base engine.

The repository contains the Obsidian theme `Doctorfree`. To use this theme with Obsidian:

- Clone or download the repository
    - `git clone https://github.com/doctorfree/Obsidian-Snippets.git`
- Create a new Obsidian vault from the folder created above
- Select the `Doctorfree` Obsidian theme
    - Go to `Settings -> Appearance -> Themes` in Obsidian
    - Select `Doctorfree` from the drop down menu of available themes

**[Note:]** Obsidian is free for personal non-commercial use but must be purchased in revenue generating operations (see the note on [Obsidian license restrictions](#obsidian-license-restriction) below).

### Markdown_viewers

Recommended markdown viewers, available for all platforms and with many features:

- [Obsidian](https://obsidian.md)
- [nb](https://xwmx.github.io/nb)

If Obsidian does not suit your needs, there are many free an open source markdown editors and viewers available for all platforms. Doctorfree uses the [nb](https://xwmx.github.io/nb/) command line and local web note-taking, bookmarking, archiving, and knowledge base application. Obsidian and nb work well together to provide a rich markdown editing, viewing, and management system. See the [Obsidian plus NB](#obsidian-plus-nb) section below for details.

Several excellent resources exist that provide lists and reviews of popular markdown editors and viewers:

- https://github.com/rhythmus/markdown-resources
- https://github.com/mundimark/awesome-markdown-editors
- http://mac.appstorm.net/tag/markdown
- http://mashable.com/2013/06/24/markdown-tools
- http://pastebin.com/j7Pjq1QT
- http://brettterpstra.com/ios-text-editors

Obsidian is pretty cool though, so try it out.

### Clone_and_view_locally

To explore this repository locally or to integrate it into a service, first clone the repository:

```
git clone https://github.com/doctorfree/Obsidian-Snippets.git
```

This will result in a local folder, `Obsidian-Snippets`, containing all of the markdown and supporting file assets. Import these into your markdown viewer. The import method varies from viewer to viewer. To import into Obsidian:

- Open another vault (or create new vault if first time)
- Open folder as vault (click "Open")
- Navigate to the `Obsidian-Snippets` folder created by `git clone ...`
- Click "Open" to create the new Obsidian vault

## Included_snippets

The default theme full CSS:

- [Default theme](Default.md)

Written by [Doctorfree](https://github.com/doctorfree):

- [Graph View Skin](Graph-view-skin.md)

### Dmytro-Shulha

Included from [Dmytro Shulha](https://github.com/Dmytro-Shulha/obsidian-css-snippets) and elsewhere:

|    |    |    |    |
|----|----|----|----|
| [Center Tables](dmytro-shulha/Center-Tables.md) | [Dracula Skin](dmytro-shulha/Dracula-skin.md) | [Text Box](dmytro-shulha/Text-Box.md) | [Animation](dmytro-shulha/Animation.md) |
| [Block quote inline](dmytro-shulha/Block%20quote%20inline.md) | [Block quote](dmytro-shulha/Block%20quote.md) | [Buttons - stylized](dmytro-shulha/Buttons%20-%20stylized.md) | [Check box](dmytro-shulha/Check%20box.md) |
| [Clutter remove](dmytro-shulha/Clutter%20remove.md) | [Command palette](dmytro-shulha/Command%20palette.md) | [Country flag hashtag](dmytro-shulha/Country%20flag%20hashtag.md) | [Edge on left](dmytro-shulha/Edge%20on%20left.md) |
| [Embeds](dmytro-shulha/Embeds.md) | [Export to PDF](dmytro-shulha/Export%20to%20PDF.md) | [File explorer - Obsidian](dmytro-shulha/File%20explorer%20-%20Obsidian.md) | [Folding arrows](dmytro-shulha/Folding%20arrows/Folding%20arrows.md) |
| [Font](dmytro-shulha/Font.md) | [Footnotes](dmytro-shulha/Footnotes.md) | [Graph nodes](dmytro-shulha/Graph%20nodes.md) | [Gutter line numbers](dmytro-shulha/Gutter%20line%20numbers.md) |
| [Headers](dmytro-shulha/Headers.md) | [HTML](dmytro-shulha/HTML.md) | [Hyphenation-Justification](dmytro-shulha/Hyphenation-Justification.md) | [Images](dmytro-shulha/Images.md) |
| [Lines - horizontal](dmytro-shulha/Lines%20-%20horizontal.md) | [Links](dmytro-shulha/Links.md) | [Lists - (un)ordered](dmytro-shulha/Lists%20-%20(un)ordered.md) | [Markers](dmytro-shulha/Markers.md) |
| [Mermaid](dmytro-shulha/Mermaid.md) | [Note title in pane](dmytro-shulha/Note%20title%20in%20pane.md) | [Outliner pane](dmytro-shulha/Outliner%20pane.md) | [Panes](dmytro-shulha/Panes.md) |
| [Popover-Popup](dmytro-shulha/Popover-Popup.md) | [Progress bar vault launch](dmytro-shulha/Progress%20bar%20vault%20launch.md) | [Resizable Mermaid](dmytro-shulha/Resizable%20Mermaid.md) | [Ribbons](dmytro-shulha/Ribbons.md) |
| [Scroll bar](dmytro-shulha/Scroll%20bar.md) | [Search](dmytro-shulha/Search.md) | [Sentences](dmytro-shulha/Sentences.md) | [Settings](dmytro-shulha/Settings.md) |
| [Sidebar](dmytro-shulha/Sidebar.md) | [Sidenotes](dmytro-shulha/Sidenotes.md) | [Special effects](dmytro-shulha/Special%20effects.md) | [Status bar](dmytro-shulha/Status%20bar.md) |
| [Table](dmytro-shulha/Table.md) | [Tag pills](dmytro-shulha/Tag%20pills.md) | [Title bar](dmytro-shulha/Title%20bar.md) | [Tooltip](dmytro-shulha/Tooltip.md) |
| [URLs](dmytro-shulha/URLs.md) | [Vim Static Caret](dmytro-shulha/Vim%20Static%20Caret.md) | [WYSIWYG](dmytro-shulha/WYSIWYG.md) | [Yaml](dmytro-shulha/Yaml.md) |

### Awesome_Obsidian

Included from [Knut Magnus Aasrud](https://github.com/kmaasrud/awesome-obsidian/tree/master/code/css-snippets):

|    |    |    |    |
|----|----|----|----|
| [Autofading ui](awesome-obsidian/autofading-ui.md) | [Better bullet points in edit mode](awesome-obsidian/better-bullet-points-in-edit-mode.md) | [Bigger link popup preview](awesome-obsidian/bigger-link-popup-preview.md) | [Bullet point relationship lines](awesome-obsidian/bullet-point-relationship-lines.md) |
| [Collapsing sidebar](awesome-obsidian/collapsing-sidebar.md) | [Custom icons differing files and folders](awesome-obsidian/custom-icons-differing-files-and-folders.md) | [Custom icons for frontmatter tags](awesome-obsidian/custom-icons-for-frontmatter-tags.md) | [Custom icons for specific folders](awesome-obsidian/custom-icons-for-specific-folders.md) |
| [Enlarge image on hover](awesome-obsidian/enlarge-image-on-hover.md) | [Hyphenation and justification](awesome-obsidian/hyphenation-and-justification.md) | [Image cards](awesome-obsidian/image-cards.md) | [Media grid](awesome-obsidian/media-grid.md) |
| [Nicer checkboxes](awesome-obsidian/nicer-checkboxes.md) | [Outliner for the outline and file explorer](awesome-obsidian/outliner-for-the-outline-and-file-explorer.md) | [Smaller scrollbar](awesome-obsidian/smaller-scrollbar.md) | [Stylish blockquotes](awesome-obsidian/stylish-blockquotes.md) |
| [Subtler folding gutter arrows](awesome-obsidian/subtler-folding-gutter-arrows.md) | [Tag pills](awesome-obsidian/tag-pills.md) | | |

### ScottKillen

Included from [Scott Killen](https://github.com/ScottKillen/obsidian-snippets):

|    |    |    |    |
|----|----|----|----|
| [Calendar emoji](scottkillen/calendar-emoji.md) | [Calendar starred](scottkillen/calendar-starred.md) | [Calendar weekends](scottkillen/calendar-weekends.md) | [Custom checkboxes](scottkillen/custom-checkboxes.md) |
| [Jesus words](scottkillen/jesuswords.md) | [Labeled nav](scottkillen/labeled-nav.md) | [Minimal tweaks](scottkillen/minimal-tweaks.md) | [Print](scottkillen/print.md) |
| [Tables](scottkillen/tables.md) | [Tabular numbers](scottkillen/tabular-numbers.md) | [Typography](scottkillen/typography.md) | |

### DustinKnopoff

Included from [Dustin Knopoff](https://github.com/dustinknopoff/obsidian-snippets):

|    |    |    |    |
|----|----|----|----|
| [Active file path](dustinknopoff/active-file-path.md) | [Adding css](dustinknopoff/adding-css.md) | [Bigger popup preview](dustinknopoff/bigger-popup-preview.md) | [Birthdays](dustinknopoff/birthdays.md) |
| [Block cursor](dustinknopoff/block-cursor.md) | [Builtin icons](dustinknopoff/builtin-icons.md) | [Bullet relations](dustinknopoff/bullet-relations.md) | [Changing fonts](dustinknopoff/changing-fonts.md) |
| [Collapsible side notes](dustinknopoff/collapsible-side-notes.md) | [Collapsible sidebars](dustinknopoff/collapsible-sidebars.md) | [Custom hr](dustinknopoff/custom-hr.md) | [Dataview table as cards](dustinknopoff/dataview-table-as-cards.md) |
| [Display tags aside](dustinknopoff/display-tags-aside.md) | [Enlarge image on hover](dustinknopoff/enlarge-image-on-hover.md) | [Fade controls](dustinknopoff/fade-controls.md) | [Folder file icons](dustinknopoff/folder-file-icons.md) |
| [Lined heading](dustinknopoff/lined-heading.md) | [List obsidian commands](dustinknopoff/list-obsidian-commands.md) | [Maintain line height footnotes](dustinknopoff/maintain-line-height-footnotes.md) | [Naked embeds](dustinknopoff/naked-embeds.md) |
| [Outliner tree](dustinknopoff/outliner-tree.md) | [Pane controls hover](dustinknopoff/pane-controls-hover.md) | [PDF export tweaks](dustinknopoff/pdf-export-tweaks.md) | [People nearby](dustinknopoff/people-nearby.md) |
| [Read file](dustinknopoff/read-file.md) | [Responsive type](dustinknopoff/responsive-type.md) | [Retrieve frontmatter](dustinknopoff/retrieve-frontmatter.md) | [Set embed height](dustinknopoff/set-embed-height.md) |
| [Status bar border](dustinknopoff/status-bar-border.md) | [Stylish quotes](dustinknopoff/stylish-quotes.md) | [Tag colors](dustinknopoff/tag-colors.md) | [Vim mode line focus](dustinknopoff/vim-mode-line-focus.md) |

## Support

- [Sponsor the Projects of Doctorfree](https://github.com/sponsors/doctorfree)

<a href="https://www.buymeacoffee.com/doctorfree"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=doctorfree&button_colour=5F7FFF&font_colour=ffffff&font_family=Lato&outline_colour=000000&coffee_colour=FFDD00"></a>
