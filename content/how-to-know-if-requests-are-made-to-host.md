Title: How To Know If A Request Is Made To A Certain Host?
Date: 2015-05-28 00:08
Category: Discoveries


Right, so this came up at work today.

The scenario was, let's say I want to know if an action
causes a request to be sent to a certain remote host,
let's say `abc.com`.

Here's how to do it:

    :::shell
    ping abc.com
to get the IP of the remote host. Let's say it's `158.85.52.72`.

Then, open a terminal, and use this command line:

    :::shell
    netstat -nputwc | grep 158.85.52.72

If you don't run it as root, it will keep on printing this message or suchsame
to screen:
(Not all processes could be identified, non-owned process info
 will not be shown, you would have to be root to see it all.)

So probably you might want to run it as root, or there may be another way
to squelch this 'info message', but I didn't find out as I only needed this thing
just for a while.

Ok so basically the idea of this is something like doing

    :::text
    tail -f PATH/TO/some_log.log

in that you want to keep monitoring in this terminal to see if a request
is made to that remote host you're interested in.

Now, in another terminal or perhaps the browser, carry out your action
while eyeballing the first terminal.

You'll see something like this flash by on the screen if some outgoing request
really did happen:

    :::shell
    tcp        0      0 10.0.2.15:36162         158.85.52.72:80         TIME_WAIT   -

What I specifically did was I just ran from another terminal

    :::shell
    wget aaa-bb-cccc.dd.abc.com

and that line from netstat showed up.

In the couple of seconds that I needed this, I didn't delve into
making the output nicer or less spammy from that irritating
'info message' that I mentioned. But perhaps someone out there has already done this
in a better/another way before.

*Shoutout to: **Farith** who was the originator of this question.*
