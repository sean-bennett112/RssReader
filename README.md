Simple RSS Reader
=================

This is a simple first attempt at an RSS Reader written in Polymer, mainly because I wanted to see what working with [Polymer](http://www.polymer-project.org/) and Google's [Material Design](http://www.google.com/design/spec/material-design/introduction.html) was like.

To install this, clone the repo, then run

```
npm install
bower install
grunt build
grunt serve
```

Still a very early attempt, with lots of things I'd like to eventually add.

From a feature standpoint:

- The ability to delete feeds
- The ability to label feeds and organize into categories
- Sorting feeds
- Viewing all new stories
- Starring stories
- Switching between viewing latest stories and starred stories for feeds
- Adding a queried feed to your list of feeds
- Adding support for non-RSS stories, such as social news feeds (Twitter, FB, G+, etc)

From an infrastructure perspective

- Re-style the base material design styles. The overall icon set is decent, and the visuals are nice, but the color scheme could be improved upon.
- Add tests! Not sure exactly how testing for web components works, but should definitely figure out if this is viable. If not, then that kills a lot of the bonuses of using web components.
- Rework the main component into more smaller components. The main rss-reader component is starting to get a bit unwieldy, and short probably be split up more.
- Normalize the interface for the google-feed element. There shouldn't be separate interfaces for queries and feed urls. The element should figure out based on the input what kind it is, url or not, and then return a normalized feed object. Currently the Google Feeds API returns different structures for the url and query calls. This should be normalized so that components using this one don't have to worry about it.

All in all, both Polymer and Material Design look pretty promising. It was surprisingly easy to get this up and running once I wrapped my head around how web components work, and the concept of 'everything is an element'.