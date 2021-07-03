- [What I want from _MY_ game engine](#what-i-want-from-my-game-engine)
  - [Platforms](#platforms)
  - [Languages](#languages)
  - [Assembly](#assembly)
  - [Libraries](#libraries)
  - [Modular](#modular)
    - [Modules](#modules)
  - [Programming Style](#programming-style)
  - [Assets](#assets)


# What I want from _MY_ game engine

I want a game engine that stands the test of time. One that I can usefully work
with for years/decades.

## Platforms

The web platform is the only platform that will remain.

## Languages

Javascript/Typescript is the winner of the language wars for the web. There is
however a _large_ ecosystem of usable code written in a variety of languages. It
would be good to be able to tap into the power of _all_ languages.

## Assembly

Web assembly is _likely_ the winner of the language inter-op war. Anything that
can be compiled to wasm can be bridged and made accessible. Zig is an
interesting language for providing this capability.

## Libraries

Every 3D engine has its own built in poorly developed math library (the 'new'
keyword is code-smell).

Every 3D engine is hella useful and hella frustating and un-intuitive in its
complexity.

A game engine should _hide_ the unpleasant and messy, and provide a clean
surface on which to work on.

My game engine will incorporate ALL libraries to become useful. The game itself
is timeless and data-only. The game has no idea of ANY 3rd party libraries.

The engine will be in _constant maintenance_ mode.

## Modular

To the degree that a module can remain independent it is better for it to be so.

Rule: No module can depend on any other module, otherwise it must be combined.

### Modules

- Math
- Logging
- String
- Random
- Noise
- (Data) Structure
- Time
- Graphic
- (User) Input
- Sound
- Search
- Asset (Management)
- Cache
- (Primitive) Lock
- database

## Programming Style

At the end of the day one is going to have to cheat and write mutable code for
performance. The OO style is _deeply_ a part of all modern game engines, and
there is no way of avoiding that tragedy today, if one wants to re-use existing
code.

RAM is temporary/mutable and _fast_, disk is permanent/immutable and is
relatively _slow_. They both exist. Somehow the temporary and fast vs permanent
and slow, remains a constant dichotomy-set in nature. Better to work with this
grain than against it.

Functional is a _style_ not an absolute constraint.

Functional likes to be thought of as _static_. It is _timeless_ programming.
HTML is a functional language that 'does nothing' on its own.

Non-functional likes to be thought of as _dynamic_. It _relies_ on time/history
and takes advantage of it. C is a non-functional language that exists to
manipulate memory (history).

## Assets

Assets are runtime reference data in various formats.

The mediatype of the asset is its primary 'bucket'.

Searching/organizing assets is a key functionality of a game engine.

How to best organize assets?

The game engine should prolly not have an opinion on this but allow for as many
organization strategies as possible.

The key is search, which implies indexing, which implies a database of some
sort. So at the end of the day a database _is_ going to be built.

A simple function that the game dev implements is the way to interface.

```typescript
const importer = () => {
  // returns list of asset descriptions
  // it is up to the game-dev to implement this how they wish
  return [{
    path: "/some/path/foo.jpg",
    type: "image/jpeg",
    foo: "some-random-searchable-fact"
    bar: ["fact1", "fact2"]
  }];
};
```

Game engine defines the shape of the asset-description and provides API for searching/retrieving assets.

