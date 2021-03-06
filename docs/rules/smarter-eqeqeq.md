# smarter-eqeqeq

This option will enforce `===` and `!==` in your code unless you're comparing between literals
or you're doing a `typeof` comparison. For those types of comparisons using strict equality is unnecessary.

The following patterns are considered okay and do not cause warnings:

```js
typeof foo == 'undefined'
'hello' != 'world'
0 == 0
true == true
```

The following patterns are considered warnings:

```js
a == b
foo == true
bananas != 1
```

To learn more about type coercion check out [Truth, Equality, and JavaScript](http://javascriptweblog.wordpress.com/2011/02/07/truth-equality-and-javascript/)

## When Not To Use It

If you're concerned about code consistency then it's best to use the built-in `eqeqeq` function.
