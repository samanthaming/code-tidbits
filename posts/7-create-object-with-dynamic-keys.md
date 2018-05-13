# ES6 Way of Creating Object with Dynamic Keys

Easier way to create objects with dynamic keys 💪

Previously, we always had to use the bracket notation to use a dynamic key. With ES6, we can finally create dynamic variable key in the object declaration. Woohoo! 🤩


```javascript
var key = '🔑';

// Old Way
var lock = {};
lock[key] = 'unlock';

// New Way
var lock = {
  [key]: 'unlock';
}
```


## Like this ❤️

**[Like this on Twitter](https://twitter.com/samantha_ming/status/975086499849953280)**

**[Like this on Instagram](https://www.instagram.com/p/Bgb5D0ZHd-o/?taken-by=samanthaming)**


## Image Download

![Download](7-create-object-with-dynamic-keys.png)
