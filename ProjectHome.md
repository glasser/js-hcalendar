## hCalendar ##

[hCalendar](http://microformats.org/wiki/hcalendar) is a microformat
for embedding semantic calendaring data in XHTML.

What does that actually mean? It means that something like this:

```
  <ul>
    <li class='vevent'>
      <abbr class='dtstart' title='20050521T200000-0700'>May 21, 2005</abbr>
      <abbr class='duration' title='PT2H'>(2 hours)</abbr>
    </li>
  </ul>
```

will render as plain text that is legible by humans reading your page,
and is at the same time completely machine-parsable.  hCalendar uses
the concepts of iCalendar (the data format behind Apple's iCal, among
other things), but allows 'events' to be embedded in ordinary HTML
pages using standard HTML tags.

## js-hcalendar ##

[js-hcalendar](http://js-hcalendar.googlecode.com/svn/trunk/hcalendar.js) is a simple JavaScript program which, when included in a
webpage, searches it for hCalendar events and builds a table-based
visual calendar. It then inserts that calendar into a <div
id='jhCalendar' /> that you put in your page. You should then style it
with your choice of CSS; I've created calendar.css and
minicalendar.css as examples.

It is  very simplistic: it  entirely ignores everything but  the start
date and the summary of the event; it doesn't even deal with the start
time. But it is easily extendable.

(js-hcalendar was once known as JSCalendar, but that name overlaps
with another excellent and unrelated project.)

## Demos ##

You can look at [a simple demo of a few random events](http://js-hcalendar.googlecode.com/svn/trunk/hcalendar.html). Note the links to switch between the two style sheets, if your browser does not support style-sheet switching. Or try a [list of holidays](http://js-hcalendar.googlecode.com/svn/trunk/holidays.html) from one of the first hCalendar sites, http://suda.co.uk/projects/holidays/, with JSCalendar injected.