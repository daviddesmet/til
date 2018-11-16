# Implementing Memoization

### What's Memoization?

> Memoization is the programmatic practice of making long recursive/iterative functions run much faster.

### How?

By caching expensive function calls such that the result returns immediately the next time the function is called with the same arguments.

Here's an example of a basic `memoize` function:

```javascript
function memoize(func) {
  var cache = {};
  return function() {
    var key = JSON.stringify(arguments);
    if(cache[key]) {
      return cache[key];
    }
    else {
      var val = func.apply(this, arguments);
      cache[key] = val;
      return val;
    }
  };
}
```

And here's a memoized Fibonacci function:

```javascript
var fib = memoize(function(n) {
  if (n < 2) {
    return 1;
  } else {
    console.log("working..."); // log every time we have to recurse
    return fib(n - 2) + fib(n - 1);
  }
});
```

Testing it out for the 1st time:

```bash
# Output from executing fib(10)
working...
working...
working...
working...
working...
working...
working...
working...
working...
89
```

Testing it out the 2nd time:

```bash
# Output from executing fib(10), notice the result is immediately returned from cache
89
```

### Words of advice

When implementing memoization, keep in mind the memory overhead since we are storing the results and it makes impractical for functions which execute quickly or that are executed infrequently, hence why is **recommended in functions that are computationally expensive**. If memory usage is a concern, a fixed size cache should be considered.