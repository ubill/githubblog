Title: Success! Landslide + DZslides
Date: 2015-05-26 19:26
Category: Tools


#### Success !

Well, right now got the desired behaviours that I wanted:

 - Embedded, horizontal-scrolling, slides in the middle of blog posts.
 - Able to launch slides in a separate window (and also go full screen if so desired.)

*That is, the behaviour of **DZslides**.*
And yet, in addition all the goodness and convenience of Python ***landslide***:

 - the slide style (theme) of landslide.
 - the syntax highlighting is possible out-of-the-box!
   So you can disregard what I said about needing to add javascript libraries
   in the previous post. Now everything is just statically generated
   and syntax-highlighted during the build.
 - did we mention that's it's in Python? And the code is hackable?
   And the command line to run it is simple, the switches are sane,
   and the config file format is nicely familiar?
 - (I only needed a command line with a few switches, didn't even need a config file.)

> After a one-time command line for setup, (this)
> > landslide slide1.md -c -l table -r
>
> (which copies the default theme to your local folder)
>
> and after
>
> - tweaking the default template's **base.html** template,
> - inlining the **style and js from DZslide's**,
> - and totally **discarding** the landslide's js[^discard]
>
> It was just this command line, all the way, again and again, after that.
> > landslide slide1.md -l table -r -t theme/ -d presentation.html



Also a couple of nice bonuses:

 - Able to be used from mobile browser too - swipe left, swipe right..

Right now though, there's no mobile-optimized CSS for this blog,
so the slides exceed the right edge of the mobile screen.
Not really too big of a problem though because:

 - as the blog does not prevent pinch zooming,
   the pages can be (albeit manually) zoomed
   until the slide fits horizontally into the browser.
 - also, the fix is known and not complicated - CSS media queries
   to have an appropriate size for the slides container,
   if the screen is narrower than n pixels.

[^discard]: We only strictly required the behaviour of DZslides,
although landslide's js provides us with a lot of additional goodies
(and hidden shortcut keys).
It is entirely possible to combine the js from landslides and DZslides -
but it is just too much work at this moment. Much worthy for a future
improvement, though.
