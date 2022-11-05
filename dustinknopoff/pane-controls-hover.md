---
title: Show Pane Header Icons on Hover
date: 2020-12-10
taxonomies:
  tags:
    - css
  kind:
    - styling
extra:
  author: ShaneNZ
---

![](https://forum.obsidian.md/uploads/default/original/2X/2/2848c023dc2a3111efecc12cffc9525e78be4493.gif)

```css
/*
    Fade the pane header controls unless hovered (just to reduce/minimise distraction) 
    does this per individual control to easily leave link and pin slightly more visible even if not hovered, and 
    as an easy way to do a snazzy transition delay stagger in and out ;)    
*/

/* not hovered ie. on cursor exit from the header */
.view-header:not(:hover) a.view-action[aria-label*="Preview"],
.view-header:not(:hover) a.view-action[aria-label*="Edit"]  { 
  opacity: 0.1;
  transition: opacity .25s ease-in-out;
  transition-delay: 0ms;
}

.view-header:not(:hover) a.view-action[aria-label*="link"] { 
  opacity: 0.55;
  transition: opacity .25s ease-in-out;
  transition-delay: 20ms;
}

.view-header:not(:hover) a.view-action[aria-label*="Pin"] { 
  opacity: 0.35;
  transition: opacity .25s ease-in-out;
  transition-delay: 40ms;
}

.view-header:not(:hover) a.view-action[aria-label*="Close"] { 
  opacity: 0.1;
  transition: opacity .25s ease-in-out;
  transition-delay: 60ms;
}

.view-header:not(:hover) a.view-action[aria-label*="More"] { 
  opacity: 0.1;
  transition: opacity .25s ease-in-out;
  transition-delay: 80ms;
}

/*  hovered ie. on cursor entry to the header */
.view-header:hover a.view-action[aria-label*="Preview"],
.view-header:hover a.view-action[aria-label*="Edit"]  { 
  opacity: 1;
  transition: opacity .25s ease-in-out;
  transition-delay: 0ms;
}

.view-header:hover a.view-action[aria-label*="link"] { 
  opacity: 1;
  transition: opacity .25s ease-in-out;
  transition-delay: 20ms;
}

.view-header:hover a.view-action[aria-label*="Pin"] { 
  opacity: 1;
  transition: opacity .25s ease-in-out;
  transition-delay: 40ms;
}

.view-header:hover a.view-action[aria-label*="Close"] { 
  opacity: 1;
  transition: opacity .25s ease-in-out;
  transition-delay: 60ms;
}

.view-header:hover a.view-action[aria-label*="More"] { 
  opacity: 1;
  transition: opacity .25s ease-in-out;
  transition-delay: 80ms;
}
```

[Original Forum Post](https://forum.obsidian.md/t/meta-post-common-css-hacks/1978/250)