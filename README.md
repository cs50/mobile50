# Features

## version 1

* Upon launch, app (if online) grabs latest metadata from server (e.g., XML, JSON, or YAML file describing available assets).
* Browse course's assets (PDFs, videos).
* View PDFs.
* Stream videos.
* Pre-download videos and watch offline.
* Search PDFs, videos by title.

# Sample Metadata

* See XML files at https://github.com/cs50/tv50/tree/master/var/cs50.tv/2016/fall.
* See http://cs50.tv/2016/fall/ for a hierarchical HTML rendering of that XML data.

_Note: additional videos (called "Shorts") soon to be added to that XML but format will be equivalent. Though we'll likely transition to our own XML or JSON or YAML format rather than cling to that XBEL format. Ideal if XML parsing is confined to a method that we can swap out for something else later. Odds are final format would still be hierarchical (equivalent to a tree) but where nodes can have multiple attributes, not just hrefs._

# Sketch of UI

Simple UITableView equivalent suffices but open to (efficiently navigable) alternatives.

## Main Screen

_On launch, user might see:_

* CS50 2016
* CS50 2015
* CS50 2014
* ...

## CS50 2016

_Upon clicking *CS50 2016*, user might see:_

* Week 0
* Week 1
* Week 2
* ...

## Week 0

_Upon clicking *Week 0*, user might see:_

* Slides [which links to PDF on cdn.cs50.net]
* Source Code [which links to an index listing on cdn.cs50.net, but can soon change to GitHub]
* Video [which links to 720p or 1080p version of video on CDN]

_Note: video exists on cdn.cs50.net in multiple resolutions. App could, e.g., stream 360p version by default. But user could alternatively click to download the 720p or 1080p version for offline viewing._
