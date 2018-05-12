# Combine Multiple Arrays Using Spread

Combine Multiple Arrays using ES6 Spread ‬🤩

Instead of using concat() to concatenate arrays, try using the spread syntax to combine multiple arrays into one flattened array👍


```javascript
let veggie = ['🍅', '🥑'];
let meat = ['🥓'];

// Old Way 
let sandwich = veggie.concat(meat, '🍞');
console.log(sandwich); // [ '🍅', '🥑', '🥓', '🍞' ]

// ES6 Way
let sandwich2 = [...veggie, ...meat, '🍞'];
console.log(sandwich2); // [ '🍅', '🥑', '🥓', '🍞' ]
```

## Like this Post

**[Like this on Twitter](https://twitter.com/samantha_ming/status/992839527969439744)**

**[Like this on Instagram](https://www.instagram.com/p/BiaB6mAhc8R/?taken-by=samanthaming)**


## Resources

- https://davidwalsh.name/spread-operator
- https://gist.github.com/yesvods/51af798dd1e7058625f4


## Image Download

![Download](14-combine-multiple-arrays-using-spread.png)
