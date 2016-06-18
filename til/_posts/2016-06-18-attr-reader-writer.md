---
layout: post
title: attr_reader and attr_writer
---
Doing a code review, I ran across another use of `attr_reader`. I've
seen it many times before, but never really stopped to think about
how it works and what it does.

In the case I was dealing with, a Class was created to generate an
sql query. I quite like the approach because
it feels well encapsulated. The `attr_reader` in this case gives access
elsewhere to be able to read a specific instance variable, the resulting
sql query. `attr_writer`, as I understand, works in much the same way,
just allowing writing to an instance variable in a different class.

I can see how this will be useful for pulling apart code into more
specific modules.
