# Extracting Arguments using Array Destructure

Happy Father’s Day!

Array Destructuring is terrific at extracting value from your arguments. So the next time you see the array bracket notation, just swap them out and use array destructuring syntax instead 🎉


```javascript
function sendLove(...args) {

  // ❌ Old way
  const hug = args[0];
  const gift = args[1];

  // ✅ Better way using Array Destructure
  const [icon, gift] = args;
}

sendLove('🤗', '🎁')
```

<br>

The first thing we’re doing is spreading our arguments, so you can get an array. Next we’re assigning them to our variables using array destructuring.

```javascript
// Step 1:
(...args)
args // [ '🤗', '🎁' ]


// Step 2:
const [icon, gift] = args;

icon // '🤗'
gift  // '🎁'
```

## ⚠️ Watch out

Note, array destructuring the parameters won't have the expected effect. It will return `undefined`.

This is because the arguments object is not an array. It's an Array-like object. That's why I did `...args` -- spreading the arguments will convert it to a real array. After that, you will be to apply array destructuring to extract the values.

```javascript
function sendLove([icon, gift]) {

  console.log(icon); // '🤗'
  console.log(gift); // undefined
}

sendLove('🤗', '🎁')
``` 

<br>

Read more about the `arguments` object here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments


## Resources

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Array_destructuring
- http://www.deadcoderising.com/2017-03-28-es6-destructuring-an-elegant-way-of-extracting-data-from-arrays-and-objects-in-javascript/
- https://gist.github.com/mikaelbr/9900818
- https://dev.to/sarah_chima/destructuring-assignment---arrays-16f
