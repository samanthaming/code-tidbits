# Print Ranges Natively in JS

Happy Mother’s Day 🌷

4 ways to combine strings in JavaScript. My favourite way is using ES6’s Template Strings. Why? Because it’s more readable, no backslash to escape quotes, and no more messy plus operators.

```js
Number.prototype[Symbol.iterator] = function*() {
  for(let i = 0; i <= this; i++) {
    yield i;
  }
};

[...3] // [ 0, 1, 2, 3 ]
[...6] // [ 0, 1, 2, 3, 4, 5, 6 ]
```

```js
// Print Ranges Natively in JS 🤩

Number.prototype[Symbol.iterator] = function*() {
  for(let i = 0; i <= this; i++) {
    yield i;
  }
};

[...5] // [ 0, 1, 2, 3, 4, 5 ]
```

## Resources

This makes use of Iterators and generators, read more about it here:
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators

I learned this from the ES6 course. It’s a paid course, but you can read the transcript free here:
- https://frontendmasters.com/courses/es6-right-parts/ranges/

This course is called ES6: The Right Parts from Kyle Simpson.
- Kyle's Twitter account: [@getify](https://twitter.com/getify)
- I watched it on [Pluralsight](www.pluralsight.com)

## Image Download

[Download](https://github.com/samanthaming/code-tidbits/blob/master/images/16-print-ranges-in-js.png)
