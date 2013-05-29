Fluent Notes
============

## High Performance Browser Networking
By Ilya Grigorik (Google)

[Slides](http://bit.ly/fluent-perf)

This guy is the master of web performance. He's Google's go-to for all of their products, highly involved in Chrome development, and contributor to SPDY and HTTP 2.0 (which will change our lives when they reach final spec and adoption).

He spent 3 hours walking us through the moment you enter a URL to the time it finishes loading and everything that happens. Very enlightening and I walked away with some very practical advice I hadn't ever read before on how to speed up our sites.

Have you heard of the "Critical Path" in PageSpeed? Run one of our sites in PageSpeed (the web-based version), go to the Critical Path Explorer, toggle the "Highlight Critical Path" button. It shows you all the resources you loaded on the page, but highlights only the ones critical to DOM rendering…. meaning, defer loading of all the other stuff so the document can load faster and the user sees something instead of a blank screen.

## How to Build a Web App
By Ohad Kravchick (NY Times/Google)

[Slides](http://sdrv.ms/16YV4Rb)

He walked through development of a single page web app (basically exactly how he built app.nytimes.com). It used a lot of JS technologies that I'll hopefully understand more by the end of the week, but wasn't all that complicated.

Two take aways:
* Install [LiveReload](http://livereload.com). You have your editor open and your browser open. Save a file and watch the screen update.
* [RequireJS](http://requirejs.org/) basically does what wp_enqueue_script does (a little less), but on the client-side. Worthwhile for us to implement because … well, we don't have wp_enqueue_script on our big sites.
