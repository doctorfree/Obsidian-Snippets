---
title: Show family members friends and places that are nearby
date: 2021-05-08
taxonomies:
  tags:
    - dataview
  kind:
    - plugins
extra:
  author: Moonbase59
---

I love location data, maps, and visualizing stuff. When I plan to travel or visit a friend or family member, I love to see “what’s near” in each person or location note. Automatically linking places and people together, so to say.

![](https://forum.obsidian.md/uploads/default/original/2X/c/cd1e190d4115a6935a5429fee51683d41cc34739.png)

* If I visit a friend, I can check if there are other friends or places of interest nearby, and we could maybe visit them together.
* I can check if other friends are near enough to do something together, maybe meet for a barbeque.
* When sightseeing, I won’t miss nearby friends, business contacts, favourite restaurants or other sights anymore.

## Goals
- Never miss anything nearby anymore.
- Have this dataview available as a template so it can be in every person, business contact, and place-of-interest note and automatically show me what’s near this place.
- No more people and location notes without location data (easily be copied from Google Maps or the like).

## Requirements

- All people/location notes must have a

```yaml
location: [lat, lon]
```

entry in the YAML frontmatter. (This syntax has something to do with YAML & JS data structure and easy parsing. The sequence [lat, lon] has been chosen for practical reasons: People are used to it and it can easily be copied from Google Maps and others.)
- _Dataview 0.3.0+_ installed.
- `moment.js` available (it currently is).
- Distance units of **m**, **km**, **yd** and **mi** must be usable and easy to switch.
- Distances must be calculated as correct straight-line distances, taking into account that Earth is not a perfect sphere but a rotational ellipsoid.
- Distances must also be available as (approximate; for speed and offline use) driving distances.
- Distances shall be shown with the unit appended but internally numeric, for easy calculation/comparison.
- Numbers shall be formatted *according to the language currently set in Obsidian* (`4,096.1` vs `4.096,1`). The OS’s system setting shall only be used if all else fails.
- Date & time strings must be easily formatable however I wish, defaulting to ISO-8601 (`2021-05-08T10:34:05+02:00`).
- Very long note title links shall optionally be shortened in Dataview table views, using my [dataview-shorten-links.css snippet](https://forum.obsidian.md/t/how-to-achieve-css-code-snippets/8474/152).
- Tags (from frontmatter only, a current Dataview restriction) shall be shown in one (comma- or blank-)separated string, not as a list.
- The list shall be sorted by distance from “here” (i.e., this note).
- The distance values shall be clickable and lead to the Google Maps Route Planner, destination already filled in, and start point taken from the current location.
- Above the table, a text line shall show the currently set “nearby” radius as well as the selected unit of measurement (`within 100 km driving distance, within 50 mi straight-line distance`), so we later know what’s actually shown in the table.

## The Code

```js
// Nearby Family Members, Friends and Places
// 2021-05-15 - Matthias C. Hormann (Moonbase59)

// set parameters (to be supplied via YAML frontmatter, eventually)
// DV 0.3.3 interprets "500000 m" as a Luxon duration,
// so we have to put nearby: '"500000 m"' and remove the ".
let nearby = dv.current().nearby.replace(/['"]+/g, '');
let unit = nearby.split(' ')[1];
let radius = nearby.split(' ')[0];
let origin = dv.current().location;

// search term as used in dv.pages()
// use "#tags" or '"folder/subfolder"' for a folder
let searchterm = dv.current().searchterm;

//======================================================================

function getDistance(origin, destination, unit='m') {
    // return distance in selected unit (m,km,yd,mi)
    var factor = 1.0;
    switch (unit) {
      case 'm':
        factor = 1.0;
        break;
      case 'km':
        factor = 1000.0;
        break;
      case 'yd':
        factor = 0.9144;
        break;
      case 'mi':
        factor = 1609.344;
        break;
      default:
        factor = 1.0;
        console.warn("getDistance: Invalid unit '%s', using 'm'. Valid units are: m,km,yd,mi.",unit);
    }

    var lon1 = toRadian(origin[1]),
        lat1 = toRadian(origin[0]),
        lon2 = toRadian(destination[1]),
        lat2 = toRadian(destination[0]);

    var deltaLat = lat2 - lat1;
    var deltaLon = lon2 - lon1;

    var a = Math.pow(Math.sin(deltaLat/2), 2) + Math.cos(lat1) * Math.cos(lat2) * Math.pow(Math.sin(deltaLon/2), 2);
    var c = 2 * Math.asin(Math.sqrt(a));
    var EARTH_RADIUS = 6371000; // 6,371 km in metres
    return c * EARTH_RADIUS / factor;
}

function toRadian(degree) {
    return degree*Math.PI/180;
}

function getDrivingDistance(origin, destination, unit='m') {
    // PREDICTED, using a factor.
    // Much faster, and no need for Internet access.
    // The U.S. predict 1.417, based on statistical analysis.
    // For Germany, I’ve found 1.3 a good value (comparing w/ Google Maps "best route")
    var factor = 1.3;
    return getDistance(origin, destination, unit) * factor;
}

//======================================================================

// Show what we will display.
dv.paragraph("List shows nearby places (within " + radius + " " + unit + " driving distance).");
dv.paragraph("<br><br>");

// get the pages
let pages = dv.pages(searchterm)
  .where(p => p.location &&
    // must be >0 so we don’t catch ourselves!
    getDrivingDistance(origin, p.location, unit) > 0.0 &&
    getDrivingDistance(origin, p.location, unit) <= radius)
  .sort(p => getDistance(origin, p.location, unit));

// create table
dv.table(["Name", "Tags", "Distance*"],
  pages.map(p => [
    // The name
    p.file.link,
    // tags (show '–' if none defined)
    (p.file.etags ? p.file.etags.join(' ') : '–'),
    // straight-line distance
    /*
    getDistance(origin, p.location, unit)
      .toLocaleString(moment.locale(), {maximumFractionDigits: 1}) + " " + unit,
    */
    // predicted driving distance and Google Maps Route Planner Link
    (getDrivingDistance(origin, p.location, unit)
      .toLocaleString(moment.locale(), {maximumFractionDigits: 1}) + " " + unit)
      .link('https://www.google.com/maps/dir/?api=1&dir_action=navigate&destination=' + p.location[0] + ',' + p.location[1]),
  ])
);

// show a small legend
dv.paragraph("<small>* Approximate driving distance; when clicked, opens a new Google Maps Route Planner window.</small>");
```

[Original Forum Post](https://forum.obsidian.md/t/dataviewjs-snippet-showcase/17847/2)