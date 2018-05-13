# Skip Values In Destructuring

Skip Values in Destructuring 🎉

You can use blanks to skip over unwanted values.

This way you can avoid useless variable assignments for values you don’t want during destructuring 👍


```javascript
// Ugh, useless variable assignments
let [a,b,c] = ['ignore', 'ignore', 'keep'];
console.log(a, b, c); // ignore ignore keep

// Use blanks to skip over unwanted values
let [ , , c2] = ['ignore', 'ignore', 'keep'];
console.log(c2); // keep
```

## Like ❤️

**[Like this on Twitter](https://twitter.com/samantha_ming/status/990301402311348232)**

**[Like this on Instagram](https://www.instagram.com/p/BiH_WV8hmHI/?taken-by=samanthaming)**


## Resources

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Ignoring_some_returned_values

- http://untangled.io/advanced-es6-destructuring-techniques/

- https://stackoverflow.com/questions/46775128/how-can-i-ignore-certain-returned-values-from-array-destructuring

- http://2ality.com/2015/01/es6-destructuring.html


## Image Download

![Download](13-skip-values-in-destructuring.png)
