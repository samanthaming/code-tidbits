# Named Parameters using Destructured Objects

Yay, Destructured Objects to the rescue 🎉 

Since JavaScript doesn’t natively support named parameters. This is a cool way around this issue. No more worrying about the specific order of inserting your arguments 👍


```javascript
// Boo, arguments must be in specific order
function meal(protein, carb, veggie){
  
}
meal('🥩', '🍚', '🥦')

// Yay, arguments can be in any order
function meal2({protein, carb, veggie}){
  
  console.log(protein, veggie, carb); 
  // 🥩  🥦  🍚
}
meal2({carb: '🍚', veggie: '🥦', protein: '🥩'}) 
```

## Community Examples

### Combining with Optional Arguments

**RanqueBenoit**: Great if some are optional arguments too! Also for default values.

```javascript
function oneFunc(options = {}) {
  let defaults = { one: 1 };
  options = { ...defaults, ...options };

  return options.one;
}

oneFunc() // 1
oneFunc({ }) // 1
oneFunc({ one: 2 }) // 2
```

_Thanks: [@RanqueBenoit](https://twitter.com/RanqueBenoit/status/1002991906685583360)_


## Resources

- https://css-tricks.com/new-favorite-es6-toy-destructured-objects-parameters/
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Object_destructuring
