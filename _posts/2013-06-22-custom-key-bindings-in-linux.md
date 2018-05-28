---
layout: post
title: "Custom key bindings in Linux"
date: 2013-06-22 02:50
comments: false
categories: [productivity, tutorial]
---

There are various ways to create custom key bindings/mappings in Linux.
This tutorial uses [xbindkeys](http://www.nongnu.org/xbindkeys/) on Ubuntu.

<!-- more -->

xbindkeys is a program that allows you to **launch shell commands with your
keyboard or mouse** under the X Window System. It links commands to keys or
mouse buttons, using a configuration file.

<img style="float: right;" src="http://i.imgur.com/j8Jo7dK.jpg?1" title="The blue button on ThinkPads">
I have a ThinkPad and my keyboard has one of those blue buttons. Might as well
put it to good use. I take a lot of screenshots, I'll use it for that.

1. Install xbindkeys  
   `apt-get install xbindkeys`

2. Create a configuration file for xbindkeys  
   `touch $HOME/.xbindkeysrc`

3. Identify the key to be used for launching the command  
   `xbindkeys --key`

   <pre><code>
   Press combination of keys or/and click under the window.
   You can use one of the two lines after "NoCommand"
   in $HOME/.xbindkeysrc to bind a key.
   "NoCommand"
       m:0x10 + c:156
       Mod2 + XF86Launch1
   </code></pre>

4. Add the following key binding to the configuration file `$HOME/.xbindkeysrc`

   <pre><code>
   "gnome-screenshot"
     m:0x10 + c:156
   </code></pre>

   or

   <pre><code>
   "gnome-screenshot --window --remove-border --effect=shadow"
     Mod2 + XF86Launch1
   </code></pre>

5. Autostart xbindkeys (without arguments) on login.
   One option is to use the "Startup Applications" tool.
