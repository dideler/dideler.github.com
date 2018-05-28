---
layout: post
title: "An Automated Yes Man"
date: 2014-02-16 19:52
comments: false
categories: [tools]
---

There's an interesting Unix command called the [yes command][yes].

<!-- more -->

> `yes` - output a string repeatedly until killed

Without arguments it repeatedly prints 'y'.
Guess what `yes no yes` outputs.

Yes is designed for automated input to prompts from interactive scripts, e.g.

```
yes | rm -i foo
```

So you don't have to pull off a Homer.

<p align="center">
  <img src="/media/drinking-bird.gif" title="The 'Drinking Bird toy' from the Simpsons episode 'King-Size Homer'">
</p>

It can also be used for simple load testing since it has high CPU usage.

Yes is part of GNU coreutils and [is still being maintained][commits].

To find out more about this yes man, run `man yes`.  
You can also check out [the source code][source]
or read a [technical report by MIT][report].

[yes]: http://en.wikipedia.org/wiki/Yes_(Unix)
[commits]: http://git.savannah.gnu.org/cgit/coreutils.git/log/src/yes.c
[source]: http://git.savannah.gnu.org/cgit/coreutils.git/plain/src/yes.c
[report]: http://trope-tank.mit.edu/TROPE-12-01.pdf
