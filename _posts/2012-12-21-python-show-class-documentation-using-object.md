---
layout: post
title: "Revealing documentation in Python"
date: 2012-12-21 20:01
comments: false
categories: [python, documentation]
---

Situation: You're doing automated data-collection using
[Selenium's Python Client Driver](http://selenium.googlecode.com/svn/trunk/docs/api/py/index.html)
but can't find any documentation online on the `Select` class. What now?

<!-- more -->

If the developers included docstrings in the class, we're in luck!
Python's `help` function shows any source documentation of the object or class
passed to it.

{% highlight python %}
>>> select_element = Select(driver.find_element_by_tag_name('select'))
>>> help(select_element)
Help on instance of Select in module selenium.webdriver.support.select:

class Select
 |  Methods defined here:
 |  
 |  __init__(self, webelement)
 |      Constructor. A check is made that the given element is, indeed, a SELECT tag.
 |      If it is not, then an UnexpectedTagNameException is thrown.
 |
 |      :Args:
 |       - webelement - element SELECT element to wrap
 |
 |      Example:
 |          from selenium.webdriver.support.ui import Select
 |
 |          Select(driver.find_element_by_tag_name("select")).select_by_index(2)
 |  
 |  deselect_all(self)
 |      Clear all selected entries.
 |      This is only valid when the SELECT supports multiple selections.
 |      throws NotImplementedError If the SELECT does not support multiple selections
 |  
:
{% endhighlight %}

Lucky me, the `Select` class contains detailed docstrings.

And if you want to see all the method names, you can use `dir(object)`.

{% highlight python %}
>>> dir(select_element)
['__doc__', '__init__', ..., 'select_by_value', 'select_by_visible_text']
{% endhighlight %}
