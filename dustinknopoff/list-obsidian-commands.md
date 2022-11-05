---
title: List of Obsidian Commands
date: 2021-05-15
taxonomies:
  tags:
    - dataview
  kind:
    - plugins
extra:
  author: Moonbase59
---

I needed a list of currently enabled Obsidian Commands (those in the Command Palette, internal plus plugins). So I thought »Why not do it using Obsidian itself (and Dataview)?«

### Commands sorted by internal Command ID

```js
const getNestedObject = (nestedObj, pathArr) => {
    return pathArr.reduce((obj, key) =>
        (obj && obj[key] !== 'undefined') ? obj[key] : undefined, nestedObj);
}

function getHotkey(arr) {
    return arr.hotkeys ? [[getNestedObject(arr.hotkeys, [0, 'modifiers'])],
    [getNestedObject(arr.hotkeys, [0, 'key'])]].flat(2).join('+').replace('Mod', 'Ctrl') : '–';
}

let cmds = dv.array(Object.entries(app.commands.commands))
    .sort(v => v[1].id, 'asc');

dv.paragraph(cmds.length + " commands currently enabled.<br><br>");

dv.table(["Command ID", "Name in current locale", "Hotkeys"],
    cmds.map(v => [
    v[1].id,
    v[1].name,
    getHotkey(v[1]),
    ])
    );
```
    

Result:

![obsidian-dataview-command-list-by-id](https://forum.obsidian.md/uploads/default/optimized/2X/9/941d1ddfba27d5caab7bc258634ac95fb017525d_2_482x500.png)

### Commands sorted by assigned hotkey

This I missed the most. Just to check if a planned hotkey combo is already taken …

```js
const getNestedObject = (nestedObj, pathArr) => {
    return pathArr.reduce((obj, key) =>
        (obj && obj[key] !== 'undefined') ? obj[key] : undefined, nestedObj);
}

function getHotkey(arr) {
    return arr.hotkeys ? [[getNestedObject(arr.hotkeys, [0, 'modifiers'])],
    [getNestedObject(arr.hotkeys, [0, 'key'])]].flat(2).join('+').replace('Mod', 'Ctrl') : '–';
}

let cmds = dv.array(Object.entries(app.commands.commands))
    .where(v => getHotkey(v[1]) != '–')
    .sort(v => v[1].id, 'asc')
    .sort(v => getHotkey(v[1]), 'asc');

dv.paragraph(cmds.length + " commands with assigned hotkeys.<br><br>");

dv.table(["Command ID", "Name in current locale", "Hotkeys"],
    cmds.map(v => [
    v[1].id,
    v[1].name,
    getHotkey(v[1]),
    ])
    );
```
    

Result:

![obsidian-dataview-command-list-by-hotkey](https://forum.obsidian.md/uploads/default/optimized/2X/8/86470033b38fd2b4ca5ec117606d210f2c4d349b_2_479x500.png)

### Notes


I’m on Linux and this is good enough for me. I leave remapping MacOS keys and/or adding nice `<kbd>…</kbd>` tags around the keys (but not the plus signs in between!) as an exercise for the reader. ![wink](https://forum.obsidian.md/images/emoji/apple/wink.png?v=9)

Anyway, it’s a good check what we have, and could well be a starting point for the [Buttons](https://github.com/shabegom/buttons) and [Obsidian Leaflet 1](https://github.com/valentine195/obsidian-leaflet-plugin) plugins to maybe invoke commands _language-independently_, using their _ID_. Because now we know it an can make a list!

(Bi- and multilingual people switch Obsidian’s language often, and it sucks that commands called up by their (locale-specific!) _name_ suddenly stop working.)

[Original Forum Post](https://forum.obsidian.md/t/dataviewjs-snippet-showcase/17847/13)