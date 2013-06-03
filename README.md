Fluent Notes
============

My ([Patrick Daly](http://developdaly.com/)) personal notes from the sessions I attended at Fluent Conference 2013 in San Francisco, CA.

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
* [RequireJS](http://requirejs.org/) basically does what [`wp_enqueue_script`](http://codex.wordpress.org/Function_Reference/wp_enqueue_script) does (a little less), but on the client-side. Worthwhile for us to implement because … well, we don't have [`wp_enqueue_script`](http://codex.wordpress.org/Function_Reference/wp_enqueue_script) on our big sites.

## Javascript at 18
By Brendan Elch (Mozilla)

[Demo of Unreal3D in Firefox with Javascript](http://bgr.com/2013/05/03/mozilla-firefox-unreal-engine-3-port/)! C/C++ code can be compiled to JS and then intepreted by azm.js and use HTML5 for console-like gameplay in the browser without plugins.

## The ABC of Data Visualization
By Irene Ross (Bocoup)

Uses d3.js to put together data. Announcing d3.chart.

## Javascript Authoring Tooling
By Paul Irish (Google)

Live editing available via Workspaces. Make a change in chrome dev tools and it updates the local file.
You can now edit Sass in chrome dev (needs a file watcher for live compiling).

DevTools can being THE editor?

Bower for package management.

Performance quick hits:

* Continuous repaint mode can help debug which things are using most paint time.
* The FPS meter gives a few performance indicators.
* Show paint rects and layer borders to help find paint issues (ex. painting on every scroll?)
* Layout thrashing details. Lots of layout and little painting?

## Show, Don't Tell
By Nellie McKesson (O'Reilly Media, Inc.), Chris Wilson (Google)

O'Reilly has built a CMS to publish long form content to many sources (print, web, ebook). Authors write in markup and choose where to publish to. [atlas.oreilly.com](http://atlas.oreilly.com)

## DesignOps: Removing friction from your front-end development workflow
by Jessica Allen (Engine Yard)

We need to schedule recurring customer/cusomter support UX meetings to find out pain points.

## How to Integrate Novice Developers into Your Team
By Elise Worthy

**Hungry Academy**

livingsocial couldn't hire enough Rails engineers, so they found 24 complete code noobs. They were paid to live in DC for 5 months and work 16 hour days.

10 months later all 24 people passed the academy. 20 people are still employed by livingsocial (83%).

**Why Beginners**

* Focus on functional diversity (ideas and backgrounds). When we are different we think different.

> A random group of problem solvers will outperform a group of the best problem solvers.

An expert will lead to one best solution. A team of experts will lead to closely associated best solutions.
A divere team will lead to diverse solutions.

Language can be taught, but not diversity.

* Autonomy - let individuals control their own diversity
* Mastery - incentive by challenge (give more than they may be able to handle)
* Purpose - make it meaningful

5 Habits of Highly Effective Nerds

* Each novice will have a technical mentor to meet with regularly
* Anytime something new is started take nothing for granted. Encourage questions.
* Ensure a regular pairing schedule preferably with more than one other person.
* Code should be systematically reviewed via "pull request"
* Jr Devs need individual learning goals with self-chosen objectives. Asses regularly.

## Rich Web Apps with Knockout.js
By Steven Sanderson (Microsoft)

* Model = server/DB
* View Model = Javascript
* View = HTML

Why use it?

* Lightweight (smaller than the others)
* IE6 compatible
* Reactive (automatically) or The Push Model
** Information updates without needing to check if it has been updated

## How to Quantify Single Page App Performance
By Rachel Myers (ModCloth), Emily Nakashima (ModCloth)

Performance has cumulative and lasting effects. Experiments have shown that slowing pages down have negative effects and when the test is over it takes time to recover. Users remember slow speeds and react the same.


Doing cool custom performance timings in GA, but I took away to intentionally render the fast parts of a page first.

## Developing Windows 8 Apps with HTML5 and Javascript
By Doris Chen (Microsoft)

Windows 8 desktop apps run on the same JS engine as IE10.

Supports media queries.

Windows Library for JS (WinJS) adds Windows 8 specific features to help connect to Windows APIs. Not required.

Use local resources (not CDN). jQuery 1.9.x and below need a custom version. 2.0 will support Windows 8.

WinJS.xhr is the promise method to access services (custom methods are available as well).

## NodeJS @ PayPal
By Bill Scott (PayPal)

Previously worked at Netflix. They built 4 completely different experiences and had 16 test cells on day one of their PS3 launch in 2010. Focus on measure/build/learn.

The UI layer is an "experimentation" layer.

He started at PayPal in 2011, and found PayPal's culture to be completely different than Netflix. There was a culture of a long shelf life and resistance to change. A text change could take 6 weeks.

When redoing PayPal he was faced with ideas of writing the application in Java and JSP and not writing any HTML. A new president, David Marcus, saw the need for change in their websites and shifted the stale culture.

They got in a room and acted like a small startup. Within a day or two they spun up a NodeJS server, started using Github Enterprise. UI guys sketched on a whiteboard and developers started to code on the fly with weekly reviews.

Keys to their development success:

* Server and UI separation.
* Using Twitter Bootstrap
* Javascript Tempalting (dust)
* They were able to make the UI portable to legacy systems

The President went on to say that Javascript was the key to turning PayPal around.

## Everything You Always Wanted to Know About Web Standards (But Were Afraid to Ask)
By Lea Verou (W3C)

W3C sets standards for most front-end except Javascript. Protocols are set my IETF.

**What does W3C do?**

Working groups write the specs. W3C sets the processes and coordinates events. They make tools and promote education.

**What is a W3C Working Group?**

* 90%ish Member companties like browser vendors & big websites
	* Funded by these companies by their annual subscriptions
* 5%ish Invited experts
* 5%ish W3C Staff

**How do working groups make specs?**

* Day-to-day
	* Mailing lists
	* IRC
	* Wiki
	* Bug tracking
* Weekly
	* Telcons
* Quarterly
	* FTF Meetings

Spec editors write the spec, often a volunteer from within the working group.

**What do the spec maturity levels mean?**

It all starts from an idea, then debate.

Possible outcomes:
* Accepted
* Rejected
* Forgotten

* From **Accepted** it goes to an Editor's Draft (ED).
* Then Working Group reviews the ED.
* The First Public Working Draft (FPWD) is then published.
* Then to Working Draft (WD).
* Then Last Call Working Draft (LCWD) - 3 weeks to 2 months.
* Then Candidate Recommendation (CR) and implementers are invited to start implementing. Two implementations need to test (ex. Webkit, Blink).
* Then to Proposed Recommendation (PR).
* Then to Recommendation (REC).

**How can I keep up?**

* Mailing lists are public
* Specs are free and public
* Telcon and F2F minutres are public
	* Open to auditing


uptodate.frontendrescue.org

**How can I contribute?**

Mailing lists and tests.

## CSS3/JS Selectors: When Your HTML5 Has No Class
By Estelle Weyl (Standardista.com)

[Slides](https://github.com/estelle/selectors/blob/master/45.html) - Lots of great pseudo class examples.

Javascript now has `querySelector` (i.e. `var el = document.querySelector('#bar')` or `var el = document.querySelectorAll('#bar')`) so stop using jQuery for it.

`>` child selector

`+` adjacent

`~` general sibling selector

You can even use `:target` to show hide things with pure CSS.

selectivizr.com for pseudo class usage in IE8

## Super Fast Design Decision-Making
By Julie Horvath (Github, Inc.) @nrrrdcore

[Resources](http://julieannhorvath.com/resources/)

1. Build
2. Deploy
3. Iterate

... get something out there fast and iterate after.

960.gs bookmarklet to overlay grid.

http://pea.rs/

CSS3 by Dan Cederholm

http://warpspire.com/kss/

juliannnehorvath.com/resources

## Adobe Brackets
By Glenn Ruehle (Adobe)
The application itself is written in all HTML/CSS/JS and is open source on Github.









































