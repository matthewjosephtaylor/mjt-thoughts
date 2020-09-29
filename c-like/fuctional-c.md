# Is it possible to have a homoiconic functional c-like?

## Syntax features of c-likes

- function calling is in the form `<function-name>(<arg-list>)`

```js
foo(arg1, arg2);
```

- function definition of the form
  `<function-name>(<arg-list>) {<...function-body...>}`

```js
// what data structure does this represent?
foo(arg1, arg2) {
  x=bar(arg1 + arg2) // not a value assignment, x is an _alias_, a _macro_
  baz(1,2,x)
  baz2(1,2,x)
}
```

To make this into a list

```js
[foo [arg1 arg2] [[bar [arg1 + arg2]]]
```

so a function is a list in the form `[fn-name [fn-args...] [fn]`

- infix notation

```js
1 + 2;
```
