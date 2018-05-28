---
layout: post
title: "Learning from John Resig and jQuery"
date: 2013-10-05 01:42
comments: false
categories: [education, software development]
published: false
---

_[This was originally posted on my old blog](https://sites.google.com/site/idelerdennis/blog/advice-from-john-resig)
and has been slightly modified._

<div style="display:inline;float:left;margin-top:5px;margin-right:10px;margin-bottom:0px;margin-left:0px">
<a href="https://secure.gravatar.com/avatar/b3e04a46e85ad3e165d66f5d927eb609?s=140&amp;d=https://gs1.wac.edgecastcdn.net/80460E/assets%2Fimages%2Fgravatars%2Fgravatar-140.png" imageanchor="1"><img alt="John Resig" border="0" src="https://secure.gravatar.com/avatar/b3e04a46e85ad3e165d66f5d927eb609?s=140&amp;d=https://gs1.wac.edgecastcdn.net/80460E/assets%2Fimages%2Fgravatars%2Fgravatar-140.png"></a>&nbsp;</div>

Meet [John Resig](http://ejohn.org). Original redditor, JavaScript ninja, YC
alum, author of two books, creator of jQuery, ex-Mozillian, and now Dean of
Computer Science at Khan Academy.

John was interviewed in June 2011 by Jared from [Startups Open Sourced](http://startupsopensourced.com).
You can [view the full interview](http://www.startupsopensourced.com/2011/06/21/john-resig-discusses-jquery-and-decision-to-join-khan-academy/)
and purchase [Jared's book for $5](http://www.amazon.com/Startups-Open-Sourced-ebook/dp/B004ZULMR6/ref=sr_1_2?ie=UTF8&qid=1307487412&sr=8-2)
which contains a lot more interviews with founders.

---

{% blockquote %}
What set jQuery apart, why did it succeed?

jQuery was the first client side library released with documentation. Prototype
[another JavaScript client side library] didn't get any documentation until 2007.
{% endblockquote %}

Documentation matters. I cannot stress this enough. It can mean the difference
between life and death for your project. Some projects can survive with no
documentation, but will have difficulty growing.

I've witnessed this with [Freeseer](http://freeseer.github.io/about/index.html).
When I joined, the project had almost no documentation, but we soon got a
Wikipedia page and a dedicated documentation site. We moved the
internal documentation from our VCS to Google Docs, moved our mailing list to
Google Groups, and logged the IRC channel. All these changes made viewing,
collaborating, and sharing much easier. The project has really grown since then
and interest has picked up. We recently got
[mentioned on O'Reilly Radar](http://radar.oreilly.com/2013/10/four-short-links-3-october-2013.html)
and [someone submitted the project on HN](http://news.ycombinator.com/item?id=6484568).

---

{% blockquote %}
How does the jQuery team work remotely and stay productive?

The main issue is with communication. The team has changed apps numerous times,
but currently they hold all meetings publicly and in IRC. All of the subteams
are responsible for maintaining their own blogs of weekly updates.
{% endblockquote %}

Communication is critical, and at Freeseer
[we let our student interns know that](http://freeseer.github.io/contribute/students.html#communicate).
During busy periods (when we have interns on the team), we hold weekly scrum
meetings over G+ Hangouts and the students will write weekly updates on their
blogs. We also have someone take meeting minutes and then post them to the
mailing list. Currently the mentors aren't very active in the updates, as the
focus is on the students. We should work on changing that and be more involved
with updates ourselves, we need to set the example.

---

{% blockquote %}
What’s the design philosophy behind jQuery?

Keep the code simple, above all else. Simple code that works with fewer use
cases is superior to more complex code that handles more use cases. Everything
must be documented. Everything is immensely clear as to what is going on.
Cross-platform compatibility is also very important.
{% endblockquote %}

[Most software is too complex](https://dideler.github.io/notes/method-of-operation).
You have the power to change that. "Less is more", "you aren't gonna need it",
and "keep it simple". You've probably heard these mantras before.

In recent years, I've noticed that the Unix philosophy has become popular again.
This philsophy emphasizes building short, simple, clear, modular, and
extendable code that can be easily maintained and repurposed by developers other
than its creators. And you notice it in mobile apps and projects all over
GitHub. Developers are creating programs that do one thing and do it well.

John again emphasizes the importance of documentation. It really is important
for both users and contributors.

Cross-platform matters a lot more for web applications than desktop applications
(in fact, I'd argue to focus on one platform if you're writing a desktop
application). Fortunately, the web makes makes it relatively easy to write
cross-browser applications if you stay away from older browsers.

---

{% blockquote %}
How are feature request conflicts or contentions handled?

If someone really wants a specific feature, it becomes their job to make the changes and improvements.
{% endblockquote %}

Whoever wants the feature gets to implement it. This is kind of similar to
[how GitHub works](https://github.com/holman/feedback/issues/430#issuecomment-25471792).
They believe that your team should work like an open source project.
As [@holman](https://twitter.com/holman) says, "What do you want to work on?
What's the best use of your time?". But don't go working on a feature without
talking to anyone about it first. At GitHub they work in small teams, and if you
can't convince anyone to work on the change with you, it's probably a bad idea
and might be a sign to go back to the drawing board.

Holman brings up another good point. "Everyone's opinion doesn't matter equally.
My opinion as a bystander just floating by a project's pull request matters much
less than the team that's been working day-in, day-out on that particular pull
for three months now." This is something I sometimes struggle with, but I'm
getting better at. I like to provide feedback and offer my opinion, but
sometimes I get carried away. The person with more experience should have more
say in the decision, but don't underestimate the fresh perspective that someone
new to the project can offer.

---

<b>5. Advice on finding/becoming the ideal coworker:</b><br>
&nbsp; &nbsp;Ideal coworker must have a deep understanding of their field and go above and beyond.<br>
&nbsp; &nbsp;Grades do not matter, it's what you do outside of class.<br>
&nbsp; &nbsp;Do not be contempt with the bare minimum.

{% blockquote %}
Are there universal traits you look for when deciding to work with someone?

Depending on the project, the person must have a deep understanding of their
field (e.g. Prototypal inheritance, functions, closures, as well as how the DOM
works, browser quirks from IE 6/7/8, etc). In general, Resig looks for people
who go above and beyond. Many students from M.I.T. were very smart and had good
grades, but they did nothing outside of class; they knew Java and LISP, but they
might not show initiative to do anything else. Looking at another candidate who
does something like building several projects in Ruby on Rails is much more
competitive and appealing to work with. Don’t be content to do the bare minimum.
GPA is not a good indication (Resig had a bad GPA in college).
{% endblockquote %}

If you're doing your undergrad, grades don't really matter when you want to
join the work force (it's a different story if you want to transfer or go to
grad school).

Have some side projects, and ...TODO

---

<b>6. Advice for students:</b><br>
&nbsp; &nbsp; Contribute to open source or open source your work.<br>
&nbsp; &nbsp; Don't work in secret, broadcast your work, be proud of it.<br>

{% blockquote %}
Advice for students?

If you contribute to an open source project, employers can see the code you
write, how well you work with others, the documentation you write, how clear
your API is, etc. Compared to someone who doesn’t have the same experience, it
becomes much easier to hire you. You can go from “just another college student”
to someone far above and beyond that. Nothing else matters except code in the
end; it’s a complete meritocracy in the software industry.
{% endblockquote %}
