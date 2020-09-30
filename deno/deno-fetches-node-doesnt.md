# Deno Fetches, Node Doesn't, So I Had to Put Node down

I spent the last 2 days of my life battling [Node](https://nodejs.org/en/) and
[Webpack](https://webpack.js.org/).

There is some weird import/require module thing that is causing the code I'm
writing that depends upon the js-ipfs /
[ipfs-http-client](https://www.npmjs.com/package/ipfs-http-client) module to
break with an error like:

```
TypeError: globals.fetch is not a function
```

As I tracked it down it appears this is due to webpack in 'node' mode.

When I run the same code, excluding webpack, it runs fine. This code also
previously ran fine in the browser.

After two days of frustration and research I've come to the unhappy conclusion
that here is a sort of endless circle of everyone wanting to pollyfill fetch,
and the webpack 'node' mode not knowing how to deal with it sanely.

## The Pain of Teaching and Old Dog a New Trick

Node does not support fetch. See this
[github issue](https://github.com/nodejs/node/issues/19393) for all the ugliness
of why.

This
[by Benjamin Gruenbaum](https://github.com/nodejs/node/issues/19393#issuecomment-629636089)
sums it up nicely

```
To be clear fetch is currently only blocked in core because it's a lot of work and effort to add to core well and there are a lot of stepping stones first (like figuring out what to do with AbortController and WHATWG streams). Fetch is not blocked in core because we don't want it in core.
```

## Deno Fetches

It turned out that the solution to my problem was to give up on node and move on
to [Deno](https://deno.land/) who does know how to
[fetch](https://doc.deno.land/builtin/stable#fetch).

To use Deno as a successful Node replacement in my vscode environment all I
needed to do so far was make the typings available via:

```shell
$ deno types > src/types/deno.d.ts
```

After that my problem went away and my code ran fine.

I also no longer needed to have webpack in 'node' mode, which feels even better.

Note that I'm using deno via feeding it a single main.js file 'transpiled' using
webpack. At the moment, I'm not interested in Deno's take on 'import urls', and
so prefer to use the webpack/npm tooling.

Deno appears to be OK with this state of affairs, and just like that I became a
Deno supporter.

## What to do with Old Dogs?

Given that fetch isn't IMHO that difficult of an API to support, _if one starts
from the proper primitives_, and Node is clearly struggling with this critical
API...I think this signals that Node is perhaps better thought of as a legacy
tool.

I personally would not invest any further effort in retrofitting this venerable
work-horse with more _modern_ concepts or APIs. Nor would I invest time
targeting it with new code. At some point it is better to let the past be, and
start building fresh with lessons learned.

Perhaps Deno will be a replacement. Better IMHO would be for several
replacements to come to the forefront. 

For now I will start training my new
(hopefully) faithful companion, and will give the old dog a much deserved rest.

Rest well old friend.
