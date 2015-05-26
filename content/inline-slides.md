Title: Inline Slides
Date: 2015-05-26 08:56
Category: Tools


At this moment, I'm trying to make iframes, inline slides, and Pelican work
together.

*And what better than to use this page itself for that purpose, and in conjunction with StackEdit?*

<iframe class="frame" width="700" height="600" style="display: block; margin: 0 auto;" src="/theme/slides/ub_iframe_embedder.html#dzslides-introduction.html">
</iframe>

### Hint: for now, in the iframe tag, use **root-relative** src URLs,
> like so: `src="/theme/slides/...html"` (note the **leading slash.**)

#### Success!

Click into the slides area and use left/right arrow keys to navigate.
On mobile browsers, it works out of the box if you swipe left and right in that
area.

No real fully-automated way for me at the moment though, I generate the slides
and put them in the `themes` (i.e. static folder of the Pelican theme)
and use a raw HTML `iframe` element in my Markdown post pointing to the slides
just like any other static resource...

But oh well, it was easier than I expected (once I got down to trying it) and
gives me the basic minimum functionality that I want.
To improve on it as time goes by, and discover things by **doing** as we go along.

(For the original front page, I have made it into a static page, you can see
it  [here](http://ubill.github.io/intro-post.html).)
