# Morality and Errors, Monads and Politics

It is political season in the US as I write this and I find my various social
media feeds bursting with political speech.

Why is that I wonder?

This article is an attempt to reason out why people seem so eager to share their
thoughts on politics.

## What is a Monad?

There is this beautiful thing in
[Category Theory](https://en.wikipedia.org/wiki/Category_theory) called a
[Monad](https://en.wikipedia.org/wiki/Monad).

In programming, a Monad is useful in instances where the _value_ of a thing is
dependant on _context_, which is how I discovered it. But to be clear it is a
_mathematical_ concept that was discovered by mathematicians first, but found to
be useful for a certain style of programming. It is a powerful way of _thinking_
and I recommend learning more about it to anyone.

One can _kind_ of think of it like programming with _imaginary numbers_ where
the _real_ numbers correspond with the _real_ world, and the _imaginary_ numbers
correspond with some _pure imaginary_ world (like say the world of mathematics
itself). Monads are a sort of gateway that allows the _imaginary_ world to
influence the _real_ world.

It is of course arbitrary which world one wants to call 'imaginary' vs 'real'.
The basic idea is to 'combine' the two worlds together in a way that allows for
both worlds to remain independent but allow one to _influence_ the other.

### Example of a Monad

```js
let myGlass = ["grape juice"]; // List Monad
myGlass.map((contents) => console.log("this is some delicious ${contents}")); // interaction between the 'imaginary' array contents, and the 'real' console
```

(technically this is a [Functor](https://en.wikipedia.org/wiki/Functor), but a
Functor 'good enough' for this example)

In the above example the _imaginary_ part is the 'grape juice' and the _real_
part is logging the contents to the console which I see with my 'real' eyes.

Or maybe you want to think of the imaginary part as the console and the real
part as the array that _contains_ the 'grape juice'. No practical difference.
The result is the same: the two worlds have been 'bridged' together so that one
remains _untouched_ but _influences_ the other. Real vs imaginary are just
arbitrary labels.

## Errors

What is an _error_?

A good definition comes from wikipedia:
[An error (from the Latin error, meaning "wandering") is an action which is inaccurate or incorrect](https://en.m.wikipedia.org/wiki/Error)

What is the correct flavor of ice cream?

The answer is 'it depends'.

It depends on the _individual_ and the _time_ and _place_ the individual finds
themselves.

Note that the answer to this question isn't _random_, nor is it _undefined_.
There _is_ an answer. The answer however sort of _hidden_ or one might think of
it as _imaginary_.

So how does one determine the answer?

One 'combines' an _individual_ with a _context_, and within that _context_ one
can gain access to the answer to the question.

Like all magical things, there is a catch. There is the small complexity that
the answer is only good _inside_ of the context, but perhaps one shouldn't look
gift horses too closely in the mouth. :)

So now this is great! We have a way to answer our question, and all is good in
the world.

## Combining Errors

But what if we have two individuals?

What is the 'right flavor of ice cream' for Alice and Bob?

This in a nutshell is the problem of politics.

Let's imagine that given the same context (time and place, say standing in an
ice-cream shop on a hot summer day) Alice would order vanilla, and Bob would
order chocolate. Now we know the 'right answer' for each but not the 'right
answer' for both.

How does one 'combine' two 'Monads'?

There are a number of ways of doing this, but the important thing to note is
that there is no guarantee that the resulting 'answer' will be to either Alice
or Bob's liking.

For example `1 + 2 = 3`.

`3` is _an answer_ to how to combine `1` and `2`, which if one squints a bit, we
can see sort of 'contains' `1` and `2` inside of it.

In the same way one _could_ choose some arbitrary combination mechanism to
provide an answer to the question of how to combine `vanilla` and `chocolate` as
we did for `1` and `2`.

If we use 'addition' then we might find that the answer is a swirl-mix of
chocolate and vanilla.

But that is just one _possible_ answer.

Perhaps we use 'multiplication' and provide both Alice and Bob two cones, one
filled with chocolate, one filled with vanilla.

Or maybe we say 'first come first served' and since Alice was in line before
Bob, then both get vanilla?

And on and on...there is no real limit to the ways to _combine_ preferences to
get 'an answer'.

Awesome. Problem solved! There are no end of solutions!

## Unintended Consequences

The 'answers' provided all have consequences, and worse, the consequences tend
to compound the more individuals are involved.

In our example above:

- Addition means that both get only _half_ of what they want, and worse are
  _forced_ to either try to 'pick out' the flavor they like in the swirl, or
  grimace and 'accept' it however they can (including throwing the whole mess in
  the garbage)
- Multiplication means that both get everything they want, but have to pay
  _twice as much_, and are force to 'throw away' or in some way 'deal with' the
  extra they don't want.
- First means that _one_ person is very happy, and one person is very unhappy
  with what they are given.

... and so on, the possible 'solutions' are endless.

Worse, there are 'winners' and 'losers' in this system. Some people _prefer_ the
particular _solution_ than others. Maybe they are rich aren't as concerned about
cost, or they find themselves first in line, or like the challenge of
'untangling the swirl' etc...

This means that the _solution chosen_ is a _competition_.

Ever choose a place for lunch with a group? By how much did you win or lose?
More interesting question: what rules governed the deciding?

## Say it Together: We are all Individuals!

(if you don't see the humor in this line, I beg you to read it until you find
it)

There are broadly speaking two solutions to this 'combining preferences' problem
as I see it.

1. Individualism
2. Socialism

The individualistic approach is to not force a single 'right answer' to the
problem, and accept the fact that morality on all things from 'right' ice-cream
flavor to 'right' person to mary is subjective and any attempt to find a 'right
answer' for _both_ Alice and Bob is at best trivial(they either agree or they
don't, and no answer is given for areas of disagreement) and at worst a
nightmarish prison. Thus _freedom_ is the primary virtue of individualism. It is
all about differences, vibrancy, and 'chaos' (no single right answer for
everyone, if the individual doesn't like the answer then the _answer_ is
'wrong')...

The socialistic approach is to 'change' the individuals to _accept_ 'the answer'
by attempting to make all the individuals _prefer the same thing_. If _everyone_
prefers vanilla ice cream, then there are no issues. Note that it doesn't matter
what one chooses for 'the answer', as long as all the individuals can be made to
accept it as their own. From first, addition, multiplication, etc.. are _all the
same_ and provide _the same result_. Do the 'math': a swirl with vanilla and
vanilla, two cones for the price of two, etc.... Wonderful if one loves vanilla.
Thus the reason why _equality_ is the primary virtue of socialism. It is all
about sameness, consistency, and 'order' (one right answer for all, if the
answer doesn't fit then the _individual_ must be 'wrong')...

Note: if one thinks that the other side _should_ think this or that way, then
I'd categorize this as a form of _socialism_. It is a tendency to desire a
_single kind of_ person, one that thinks 'the right way' about things, no-matter
what that 'right way' is. Doesn't matter what 'the right way' is, any single way
is an arbitrary choice between addition, multiplication, etc. being _the_
preferred solution.

## Arm-chair Psychology

This I think answers the question as to why my more 'socialistic' friends are
the ones so enamored with 'pushing' the acceptance of 'values' from
'authorities' on others, and are so threatened by any challenge to those
'authorities'. And not just a little. In my experience they feel _personally
threatened_ by any challenge to any authority they are enamored with.

Conversely, my more 'individualistic' friends usually _don't_ engage in as much
political speech (except perhaps to speak out against being pushed around by
'socialists')). Here it is the opposite, with a fierce resistance and skepticism
to any authority.

Humans are inconsistent, and I find most people in life to lie somewhere along
the _spectrum_ of individualism -> socialism.

By far, the socialists are more vocal in my experience, which makes sense given
their innate existential need to force agreement on 'a solution'. I feel this
balances exactly with the existential need of individuals to reject any single
solution, and the 'deafening silence' and disengagement I _don't_ here from my
individualists friends.

## Minor point on Socialism in the United States

As some may have guessed/known I tend to lean heavily towards individualism.

In the US there is somewhat of a stigma attached to socialism. I find most
socialists I run across shy away from the label, often to the point of what is
in my eyes self-delusion. I want to make clear that I personally don't find
socialism to be 'bad' or 'evil'. It is a legitimate way of being, and works as a
practical solution. Individuals have preferences, and as I don't dwell on why
some like vanilla when chocolate is clearly superior, I've found it best to
simply accept that some prefer things different than myself.

To my socialist friends I want you to know that one of the things I love in life
is enjoying the differences in things. I know you are different than myself, and
want you to know that I more than accept this, I enjoy living in a environment
full of individuals that hold different thoughts and ideas.

## Nature Prefers Both Individuals and Societies

Strange. There appears to be a natural competition between individualism and
socialism with no 'winner' in this endless battle.

Looking around there appears to be a sort of 'fractal balance' between the two
all through nature.

It goes in humans from humans -> nation-states->human
organism->organs->cells->organelles->....

Each category can be seen as a sort of 'individual contained within a society of
those individuals'.

## Plural vs Singular

Ever had a hard time naming a directory? Is it Image or Images? Download or
Downloads?

Is it human or humanity?

The weird thing is that this difficulty is continued at every level. Inside the
'Download(s)' directory those files have identifiable 'parts' within them. And
those parts have parts, and so on until one gets down to the 'atomic level' of
the byte...which contains bits. As a programmer I can't see anything beyond the
bit, but this is merely a limitation of current hardware. At some point qubits
will emerge...and so on and so forth.

Seeing an 'individual' or a 'group' is somewhat arbitrary and context sensitive
(what do I need to work with right now to get whatever it is I want to
accomplish done?). The answer to human vs humanity is only discoverable _in
context_.

## Monads all the way down...

What is the right length for a giraffe's neck?

What is the right set of laws and legal framework?

Who is the right person to be the president of my HOA?

I have my opinion on each of these things. They might be strongly or weakly
held, but they aren't arbitrary. Likely they are different than yours in some
small or large degree.

The individual giraffe doesn't get a choice of neck size. I live inside a
country with a given set of laws and legal framework that would be monumentally
difficult for me to challenge or hope to influence. If I campaign hard enough I
might _just_ have enough influence to sway the minds and hearts of my fellow
home owners, in choosing a minor candidate for office, that I don't find too
unpalatable.

One answer is that _natural selection_ decides. It does this by allowing us the
ability to perceive only those answers that were capable of continuing in time,
with the more 'fit' answers becoming ever more dominant.

I say it this odd way (allowing ability to perceive) because there is a funny
thing in physics. Nothing is 'real' in the way one may naively think. It is sort
of like physics embraces Monads as a way of doing its thing. It needs some
_context_ to get any sort of _real_ value.

[Is it a particle or is it a wave?](https://en.wikipedia.org/wiki/Wave%E2%80%93particle_duality)

[Who's clock is right?](https://en.wikipedia.org/wiki/Principle_of_relativity)

There is a sort of 'real' and 'imaginary' part of the universe, with
consciousness entities like humans being limited to perceiving the 'real' one.
Countless experiments have shown that the 'imaginary' part is out there, and
that there is a bridge between the two that allows the 'imaginary' to influence
the 'real' part.

Note that I'm a good physicalist and buy into relativity and quantum mechanics.
Nothing 'spooky' going on, the physical universe just has some odd aspects to it
that humans only just became aware of in the last century or so.

Therefore it is conceivable (via the many-worlds interpretation of QM) to think
of _all_ answers being tried, and in some universes Alice is happy, some only
Bob is happy, some neither, some both. The one that Carol (Alice and Bob's
child) observes many years later is impacted more by which ice cream flavor gave
the sum-total best odds of her being conceived and living to the age where Alice
and Bob could tell the tale of what flavor(s) they received).

If I had to put money down, this 'evolutionary solution' would be the 'dominant'
answer I'd bet on seeing emerge. The answer I'd _prefer_ is the one where Alice
and Bob are happy AND not too much ice-cream goes to waste. I'm encouraged that
nature does not appear to like waste, and encourages variety, and so have hopes
that pleasing-to-all solutions with allowances for many tastes can be
random-walked into.

Note that I see the 'decisions' of which ice-cream flavor is 'chosen' as
effectively a random walk (many-worlds encourages me to think this way). Which
is one reason why I prefer to encourage worlds where _many_ solutions are tried.
I desire to allow nature enough space to figure out what works and what doesn't.
Not that my preference makes any difference, as I believe this is how nature is
'solving the problem' already (I'll point to my inability to order mold-flavored
ice-cream on Amazon as 'proof' that nature is culling the weak and promoting the
strong).

The only _real_ difference is which universe I discover myself perceiving in.
I'm betting that I can 'up the odds' of landing in a more pleasant moment by
working on these words now being written.

## Call To Action

To the degree I have any influence on others I would urge you to put as much
effort into what you think are the 'right' things are as possible.

Hopefully that means more thoughtful social media posts :) but I urge
'thoughtful action towards the good' in all activities in general.

I will note that social media platforms do not make it easy to silence and
filter _particular_ speech from a person I follow (hopefully this will change as
technology improves). I have only a very broad way to filter _all_ content from
a speaker. Sadly I've found I need to do this from time to time and it always
pains me to 'throw the baby out with the bath water'.

As a hint to those wishing to engage in political speech: I personally respond
better to why something is _attractive_ than why something is unattractive. I
think this response is a natural human inclination, so I'd recommend focusing on
the _positive_ things you want individual(s) to be persuaded towards vs any
_negative_ thing you want individual(s) to be persuaded against. If all I see is
ugliness I turn off the channel entirely. If I see something beautiful or
interesting I'm naturally attracted to it, and want more.

For the record I think a giraffe's neck _should_ be about 6' in length, but that
is just me being me, feel free to differ.
