# When NO name is the Best Name

As a developer I find thinking of the best name for something is an activity I
give _particular_ importance to.

As I mentioned in a [previous article](../art/all-art-contextual.md) I view
programming more as _world building_. Similar to a fiction-writer creating a
'fictional world' for their readers.

Just as a fiction-writer spends time naming people, places, and things in their
world I spend time naming variables, and functions, and modules.

As a person who has been 'naming things' for decades I can say with confidence
that this _critical_ task never appears to get easier.

In fact, it gets _more difficult_ with time as my depth of knowledge and range
increases. It was simpler when I was a wee-programmer and my 'vocabulary' was
more limited.

This is going to sound silly: I've now reached a point where I revere the naming
of things to such a degree that I often _dare not_ name some things.

For example, I find I want to write code more like this

```js
const uppercase = (value) => value.toUpperCase();
["red", "green", "blue"].map(uppercase);
```

vs this:

```js
const uppercase = (value) => value.toUpperCase();
["red", "green", "blue"].map((color) => uppercase(color));
```

(removes the extra name `color`)

I often edit code with 'extra names' to make it more terse. Almost never the
other way.

The advantage is that this code is now more flexible and can be used in many
more _contexts_.

```js
["small", "medium", "large"].map((color) => uppercase(color));
["small", "medium", "large"].map(uppercase);
```

Note above the name 'color' rather than _illuminating_ what is going on and
'filling out' the story, does just the opposite and introduces a confusion,
perhaps even a _lie_. The more terse 'nameless' version is in some sense
'better'.

Of course the same problem exists with any name

```js
const uppercase = (value) => value.toLowerCase();
["red", "green", "blue"].map(uppercase);
```

When I name something I have to be _very careful_ that the name _agrees_ with
that the _reader_ thinks that name _means_.

This 'agreement' between the reader and the writer is the problem. Problems
arise even when the reader and writer are _the same person_ (perhaps before and
after lunch), much less if other individuals in a team environment, or random
person on the internet, need to come to agreement.

## It would be nice to get rid of names altogether

Unfortunately this makes the code as 'unreadable' as a fiction-writer writing a
story with no names for the characters, places, things, etc... Doable perhaps,
but I doubt if the reader would enjoy the experience.

The human mind is limited, and _needs_ names to make sense of the world.

## Naming is Hard

The sad fact is that names are a _hard_ part of programming and take constant
care and attention. In balance, they are also where much of the _meaning_ and
_joy_ come from.

When naming, to a degree it depends on who the _target audience_ is and what
_they_ think a name means or represents.

When I say 'foo' paired with 'bar' those names _represent_ something in
particular to one audience, and might be meaningless dribble to another.

When I say 'map' it gets trickier because the word has 'many meanings' in 'many
contexts' to 'many audiences'.

However, if I can _get away_ without using _any_ name, that is an elegant
solution that fits almost anywhere.

## Standard Names are Nearly Invisible

I recommend to _read widely_ and examine as much code as one is able. If a name
crops up repeatedly, then I do my best to take note of it, especially how it is
being 'implicitly defined via usage'.

Thus a vocabulary is built up over time that allows one to _speak_ to other
code-writers in a language that is _understandable_ to code-writers.

This helps by using a 'standard' name for something, taking the burden off of
both the writer and the reader.

A `for loop` that didn't use `i` for the counter would be _harder_ for most 20th
century c-like language readers to read.

I find that standard names are the next best thing to a 'no-name'.

## Conclusion

I don't believe there is any 'right' answer to the question when or how to name
things. Similar to how there is no 'right' answer to how any story-author should
name things in their world.

'Not naming' is a valuable _tool_ in the naming-toolbox.

I note that _not-naming_ is a trick many world builders use in writing.

Often I find stories with _fewer_ names to keep track of, have more of a
_timeless_ quality. Stories with _more_ names I find have a more _immediate_ and
_real_ quality to them.

It think the same holds for naming in programming. To the degree that the
program needs to be _timeless_, fewer names are desired. To the degree that the
program is a _one off_, _custom_ or wants to fill a particular _immediate_ role,
more names are called for.

With this in mind, I think it is best to err on the side of _too many_ names,
and then _edit down_ the names as the code evolves over time. I also find this a
natural inclination, and thus easier to achieve and remain consistent with. The
names that survive many 'cullings' over time I find take on deeper meaning and
purpose, and thus _earn their keep_.
