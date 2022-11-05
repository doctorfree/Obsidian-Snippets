---
title: Upcoming Birthdays
date: 2021-05-09
taxonomies:
  tags:
    - dataview
  kind:
    - plugins
extra:
  author: Moonbase59
---

Here’s a rather robust and flexible list of upcoming birthdays that

-   shows **link**, **next birthday**, and **age** someone will turn to
-   has a configurabe **date range** (from today, for a “natural language” duration)
-   sorts by **next birthday**
-   uses **locale settings** from the language _Obsidian is set to_
-   doesn’t choke when crossing the year boundary
-   has YAML **searchterm** configuration
-   has YAML “natural language” **duration** configuration; “odd” data like `duration: 0.5 years` will be auto-translated to `6 months` (or `6 Monate` in German)
-   has YAML **date format** configuration (yay!)
-   has a configurable **info line** above the table (can be disabled)

![obsidian-dataview-upcoming-birthdays](https://forum.obsidian.md/uploads/default/optimized/2X/4/4f70d33649d6c45a7ac9c86b3226b0cb3f021dc0_2_690x487.png)

  
Upcoming birthdays with English settings, custom date format and info line

**The technically-minded** may also find interesting:

-   utility functions that can be used for table data
-   custom function for “where”
-   comparator function for “sort”
-   easily translatable “info line” with parameters
-   how I need to _undo_ Dataview’s YAML pre-parsing of dates and durations

![obsidian-dataview-upcoming-birthdays-de](https://forum.obsidian.md/uploads/default/optimized/2X/5/5d6ccde0ae290500f38c930b2c91142f45f27304_2_690x483.png)

  
Upcoming birthdays with German settings, custom date format and info line

## Requirements


-   _Dataview 0.3.3+_
-   `moment.js` (comes with Obsidian)
-   Notes to be included must have a birthday as `YYYY-MM-DD` in the frontmatter:
    
        birthday: 1959-07-19
        
    
-   The note _using_ this script **must** have the parameters `searchterm` and a (more or less) “natural language” `duration` in the frontmatter:
    
        #searchterm: "#family or #friends"
        searchterm: '"People"'
        duration: 1 year
        
    
-   The note using this script **_can_** have an additional `dateformat` in the frontmatter:
    
        dateformat: "ddd, D MMMM YYYY"
        
    
    If left out or empty, it will default to `YYYY-MM-DD`.

## Code

### YAML frontmatter example

```yaml
#searchterm: "#family or #friends"
searchterm: '"People"'
duration: 1 year
dateformat: "ddd, D MMMM YYYY"
```

### `dataviewjs` code

This contains some utility functions that can be used in your table, like `nextBirthday()`, `turns()`.

```js
var start = moment().startOf('day');
var end = moment(start).add(dv.current().duration);
var dateformat = "YYYY-MM-DD";
if (dv.current().dateformat) { dateformat = dv.current().dateformat; }

// info text above table, {0}=duration, {1}=start date, {2}=end date
// parameters can be left out, or the string empty
var infotext = "Upcoming birthdays for {0} from now ({1} – {2})<br><br>";

//======================================================================

function nextBirthday(birthday) {
    // Get person’s next birthday on or after "start"
    // returns a moment
    
    // need to "unparse" because DV has already converted YAML birthday to DateTime object
    // shouldn’t harm if already a string
    var bday = moment(birthday.toString());
    var bdayNext = moment(bday).year(start.year());
    if (bdayNext.isBefore(start, 'day')) {
        bdayNext.add(1, "year");
    }
    return bdayNext;
}

function turns(birthday) {
    // Get the age in years a person will turn to on their next birthday

    // need to "unparse" because DV has already converted YAML birthday to DateTime object
    // shouldn’t harm if already a string
    var bday = moment(birthday.toString());
    return nextBirthday(birthday).diff(bday, 'years');
}

function showBirthday(birthday) {
    // Determine if this birthday is in the range to be shown
    // including the start date, excluding the end date
    // because that comes from a duration calculation
    // for use with "where", returns true or false
    
    if (birthday) {
        // need to "unparse" because DV has already converted YAML birthday to DateTime object
        // shouldn’t harm if already a string
        var bday = moment(birthday.toString());
        var bdayNext = nextBirthday(birthday);
        if (bdayNext.isBetween(start, end, 'day', '[)')) {
            return true;
        } else {
            return false;
        }
    } else {
        return false;
    }
}

function sortByNextBirthday(a, b) {
    // comparator function for "sort"
    
    if (nextBirthday(a).isBefore(nextBirthday(b))) {
    return -1;
    }
    if (nextBirthday(a).isAfter(nextBirthday(b))) {
    return 1;
    }
    // they’re equal
    return 0;
}


//======================================================================

dv.paragraph(infotext.format(moment.duration(dv.current().duration.toString()).humanize(), start.format(dateformat), end.format(dateformat)));

dv.table(
    ["Name", "Birthday", "Turns"],
    dv.pages(dv.current().searchterm)
        // use a function to see if this birthday is in range to be shown
        .where(p => showBirthday(p.birthday))
        // use a comparator function to sort by next birthday
        .sort(p => p.birthday, 'asc', sortByNextBirthday)
        .map(p => [
            p.file.link,
            p.birthday ? nextBirthday(p.birthday).format(dateformat) : '–',
            turns(p.birthday)
        ])
);
```

## Notes


-   Dataview actually _parses_ the cell content, so if you for example set the date format to `D. MMMM`, you’ll get large vertical spacing. This is because DV _thinks_ something like `17. May` must be an _ordered list item_ and parses it accordingly. Which in turn will ruin your vertical spacing.  
    See [0.3.3: table item converts to ordered list, ruining vertical spacing · Issue #199 · blacksmithgu/obsidian-dataview · GitHub 1](https://github.com/blacksmithgu/obsidian-dataview/issues/199).
    
-   Using durations > 1 year (like `2 years`) _work_, but don’t make much sense. The table will only display a person’s _next_ birthday. So no duplicates.

[Original Forum Post](https://forum.obsidian.md/t/dataviewjs-snippet-showcase/17847/6)