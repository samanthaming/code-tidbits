# Print Ranges Natively in JS

One of my favorite feature of Ruby is ranges. But it’s not natively available in JS. That’s about to change! Learning ES6 from [@getify](https://twitter.com/getify) 🤩

Add this snippet to print ranges in your number prototype!

```javascript
Number.prototype[Symbol.iterator] = function*() {
  for(let i = 0; i <= this; i++) {
    yield i;
  }
};

[...3]; // [ 0, 1, 2, 3 ]
[...6]; // [ 0, 1, 2, 3, 4, 5, 6 ]
```

## Examples

You can even apply your standard loop methods on it!

### Using it with Map

Use it with the map method to triple each of the number.

```javascript
const triple = [...3].map(x => x * 2);

triple // [ 0, 3, 6, 9 ]
```

### Using it with Filter

Combine it with the filter method to get rid of the odd numbers. (by the way, nothing wrong with odd one 😉)

```javascript
const even = [...10].filter(x => x % 2 === 0);

even; // [ 0, 2, 4, 6, 8, 10 ]
```

## Resources

- I learned this from a course on [Pluralsight](www.pluralsight.com). It's called ES6: The Right Parts from Kyle Simpson. 

- It is a paid course, but I found a free transcript [here](https://frontendmasters.com/courses/es6-right-parts/ranges/).

- This code recipe makes use of Iterators and Generators, read more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators)


## Image Download

[Download](https://github.com/samanthaming/code-tidbits/blob/master/images/17-print-ranges-natively.png)
