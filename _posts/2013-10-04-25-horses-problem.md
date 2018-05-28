---
layout: post
title: "25 Horses Problem"
date: 2011-11-27 13:00
comments: false
categories: problems
---

_[This post was migrated from my old blog](https://sites.google.com/site/idelerdennis/blog/25-horses-problem-palantir)
and has been slightly modified for improved readability._

<!-- more -->

---

<small>**Update (March 2012):** Terry Ng found an error in my original solution.
In the step before the final race, I eliminated all horses with a 3rd place
finish from the first 5 races, this included horse W. Instead we should
eliminate horse G, as explained in this updated version of the solution.
</small>

Earlier this week, a technical sourcer from
<a href="http://www.palantirtech.com/" target="_blank">Palantir</a> contacted me
after she noticed <a href="http://www.linkedin.com/in/dennisideler"
target="_blank">my LinkedIn profile</a>. She said it was impressive for someone
who's still in school and she would like to have a brief chat with me regarding
career opportunities.

So I started reading about Palantir, including
<a href="http://www.businessweek.com/magazine/palantir-the-vanguard-of-cyberterror-security-11222011_page_1.html">this article</a>
which appeared in my Twitter feed.  On the 5<sup>th</sup> page,
there's an example of an interview question that Palantir may ask.

<blockquote>
You have 25 horses and can race them in heats of 5.<br>
You know the order the horses finished in, but not their times.<br>
How many heats are necessary to find the fastest?<br>
First and second? First, second, and third?<br>
</blockquote>

Cool, I enjoy solving puzzles. I'll attempt it! And so began this journey...

<h4>8 Balls Problem</h4>

This question reminded of the <q>8 balls problem</q>.
For those not familiar with it, I made this drawing.<sup>[[1]](#f1)</sup>

<img
src="https://docs.google.com/drawings/d/1jYRd_hoKBvEHQBV1W4Ub8v_QDryh7e-9yfkpvRNj2Ac/pub?w=1114&amp;h=1927">

<h4>Investigating The 25 Horses Problem</h4>

The <q>25 horses problem</q> is kind of similar:

<ul>
  <li>There's a given amount of items</li>
  <li>One item stands out from the rest and you have to find out which</li>
  <li>You can group the items and gain limited information at each step</li>
  <li>How many steps are necessary to find the correct item?</li>
</ul>

The key differences are that in one problem (8 balls)

<ol>
<li>you count the number of steps (weighings - 2 groups at a time)</li>
<li>you choose your group size (both groups must have the same size)</li>
</ol>

whereas in the other problem (25 horses)

<ol><li>you count the number of groups (races)</li>
<li>your group size is fixed and given</li>
</ol>

So they're different optimization problems. The 25 horses problem also goes
a few steps further, because not only does it ask for the first item, it also
asks for the second and third item.


The posed question is a bit confusing, and having no interviewer to clarify
doesn't help. A horse is not consistently the fastest. A horse that wins one
race, may not win its next. In other words, the fastest horse changes every race
if measured by order they finish in. If measured by time, the fastest horse does
not change (until the fastest record is broken). But since time is out of the
question, let's just ignore time completely.

<h4>Attempt</h4>

<img
src="https://docs.google.com/drawings/d/1JBv-Ct31VpHRzJKbuTIu0t8ClK7M9xRjEpVAYXupcJw/pub?w=1120&amp;h=2186">

<h4>Conclusion</h4>

With the (supposedly correct) answer in front of you, the problem seems simple.
But admittedly I had a tougher time with this problem than I anticipated. That
probably came from initially thinking that it was very similar to the <q>8 Balls
Problem</q>.

If I were asked this during an interview, I'm not sure if I would get it right
on the spot. It's a tricky problem and I'd of course be nervous because of the
time constraints and the risk of missing a career opportunity if I screw up.
I would definitely be using a whiteboard or a piece of paper as a visual aid,
makes tackling such problems a lot easier.

<section id='f1' />
<sub>
[1] In the actual task, the balls look identical.
</sub>
