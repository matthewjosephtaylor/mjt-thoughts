# Is async/await harmful?

After a few months of programming using the async/await style of dealing with
Promises I've come to a tentative conclusion that I don't like async/await.

One problem is when problems (Exceptions) arise. One is _tempted_ to simply
ignore exceptions with async/await. Forget that errors are even a possibility.

```js
async function foo(): Promise<string> {
  const bar = await someProcess();
  const baz = bar + " something insightful";
  return baz;
}
```

What happens when someProcess() fails? Who knows/cares. We are safe within our
Promise and can rest assured that the failure will magically result as a
'reject'.

The syntax/style _leads_ one to forget that one is working in an
Exception-oriented error-space. Worse is the ugliness of the try/catch syntax
that is encouraged for dealing with exceptions with await.

```js
async function foo(): Promise<string> {
  try {
    const bar = await someProcess();
    const baz = bar + " something insightful";
    return baz;
  } catch (reason) {
    // what to return here for the 'error' value?
  }
}
```

If one deals with exceptions using the Promise::catch it isn't much better

```js
async function foo(): Promise<string> {
  const bar = await someProcess().catch((reason) => {
    // what to return here for the 'error' value?
  });
  const baz = bar + " something insightful";
  return baz;
}
```

The other more _frustrating_ problem is _forgetting_ to add `await` before a
function.

The function maybe didn't _used_ to return a promise, but now it does, and
because it does the _caller_ has to be aware.

```js
async function foo(): Promise<string> {
  const bar = someProcess();
  const baz = bar + " something insightful";
  return baz; // no type errors even though it is clearly not right
}
```

## Conclusion

I'm going to give async/await a miss for a bit and see if this brings more joy
to the art of programming.

I'm also encouraged with this change to fully embrace the FP style of
programming in Typescript. Async/await I think is a clever crutch, and still has
its place for short/simple 'one off' things, but anything deserving real
attention wants a more thoughtful approach.

To that end I've started creating my own Monads and such here
[typescript-monad](https://github.com/matthewjosephtaylor/typescript-monad).

Somewhat as a learning tool to help me master the Typescript typing system, and
also to come to deeper grips with the world of Monads, and somewhat because I
have _opinions_ on how I desire these things to work. :)

I'd be curious to know others opinions on async/await and if they've come to
resolve their issues they might have, or reject them entirely as I'm attempting?
