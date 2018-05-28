---
layout: post
title: "Boolean Hacks in C"
date: 2010-09-27 21:21
comments: false
categories: [c, hacks]
---

You're used to Booleans as logical or truth values but you miss them in _C_.
You'd like your code to be more verbose and readable instead of 1's and 0's all
over the place.

Here are some simple workarounds I've found over the years.
Most of these take advantage of chars being an
[integral data type in C](http://en.wikipedia.org/wiki/C_syntax#Primitive_data_types)
(i.e. they are stored as integers).

<!-- more -->

#### Method 1: by Unknown
```
typedef unsigned char bool
const true = 1;
const false = 0;
```

#### Method 2: by Unknown
```
#define true 1
#define false 0
typedef unsigned char bool
```

#### Method 3: by Julian Assange in [strobe.c v1.03](http://stuff.mit.edu/afs/athena/contrib/potluck/src/strobe/strobe.c)
```
#define bool char
```

#### Method 4: by Julian Assange in [strobe.c v1.05](ftp.kfki.hu/packages/security/COAST/scanners/strobe/strobe/strobe.c)
```
#define bool int
#define FALSE 0
#define TRUE 1
```

#### Method 5: by Daniel Fredouille in [C generic data structures](http://www.comp.rgu.ac.uk/staff/df/down/prog/doc/Cstructures/group__bool.html)
```
#define true (0==0)
#define false (!true)
typedef unsigned char bool
```

#### Method 6: by Qhull in [libqhull.h](http://gitorious.org/qhull/qhull/blobs/master/src/libqhull/libqhull.h)
```
#define bool unsigned int
#ifdef False
#undef False
#endif
#ifdef True
#undef True
#endif
#define False 0
#define True 1
```

Do you know of any others? Send them to me and I'll post them here!
