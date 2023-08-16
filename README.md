Ok, so here is a good question to structure our <sputtering, but hopeful> association with:

1.  In the building out of our courses and labs, we have the slides component already selected, it's Google Slides, so that's sorted
2.  Labs are currently in text, and very simplistic, and I'd like to avoid us having to institute a whole content management system around labs, other than using git to keep revisions etc.
The issue is that Markdown has limitations about how we can highlight keywords inside \``` fencing, which we are using as the commandline output block, either white text on black background or reversed.
3.  I have seen places in the docs where highlighting is applied to text in ways that I can't explain with the \``` fencing and a language, such as json after the \```.
4.  If we could have a way to highlight a single word, or entire code sample line while still following git markdown rules, we could just use git for our lab-writing and revision control.
5.  As it is, git doesn't highlight differently with code and triple \``` since it just shows one as an inline `code` and the other in triple \``` fencing as a code block, but the same color scheme.
6.  This is not optimal, we'd like to have the ability to colorize \``` fenced blocks as well as highlight words inside those blocks.

That's an apparently small thing, but if we can somehow manage to represent our labs in Markdown or Markdown+something that lets us do highlighting properly, we can avoid having to use a word processor (shudder) to format our labs in an appropriate way.

Below is an example of what I am talking about.

**Steps**

1. do the ls thing

    `ls -la /etc`

```
drwxr-x---+ 21 rossb  staff    672 Aug 10 15:56 .
drwxr-xr-x   5 root   admin    160 Jul 26 12:43 ..
drwx------+  8 rossb  staff    256 Aug  8 16:45 .Trash
drwxr-xr-x@  3 rossb  staff     96 Jul 25 11:11 .config
drwx------   3 rossb  staff     96 Jul 25 06:50 .cups
drwxr-xr-x@  5 rossb  staff    160 Jul 26 11:20 .vscode

```

In the above output, notice the **.cups** directory, which we'd like to either independently highlight just the `.cups` word or the entire line, but can't figure out how to do that within the fencing.  I've tried language, which doesn't highlight what we want, I've tried all kinds of \` contortions, nothing has worked.

I've talked with John Gruber himself (inventor), and Matt Cone, the Markdown book author, no dice.

I've seen how you're using what appears to be this kind of highlighting in the docs, in particular on this page:

https://grafana.com/docs/grafana/latest/cli/

For example, they've highlighted just individual words or phrases with a different color, such as the `-h` in the **Display Grafana CLI help** section.

I know some of this can be done using the language tag right after the \``` fencing starts, but this doesn't allow us to make our own specialized "hightlight this word or phrase" style, where in a word processor or markup language we just apply the tags and Voila, it's highlighted.

Love to get your thoughts on how we could do this, and keep things as simple as possible, but still be very effective when we want the lab-taker to notice something either in input or output.

Ross
