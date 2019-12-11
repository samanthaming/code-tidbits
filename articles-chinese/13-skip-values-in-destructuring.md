Translated by [@baooab](https://github.com/baooab)

# 在解构赋值中跳过值 🎉

你可以使用空格跳过不想要的值。

这样的话你就可以在解构时避免无用的变量赋值 👍

```javascript
// 看，无效的变量赋值
let [a,b,c] = ['ignore', 'ignore', 'keep'];
console.log(a, b, c); // 忽略 忽略 保留

// 使用空格跳过不想要的值
let [ , , c2] = ['忽略', '忽略', '保留'];
console.log(c2); // 保留
```

## 社区建议

### 使用注释提高代码可读性

你可以在空白区域内使用注释，使你的代码更具可读性。这有助于向你的小伙伴传达你是故意跳过不需要的值。

_致谢：[@sulco](https://twitter.com/sulco/status/990952399060832257)_

```js
let [
  chili,
  , // rotten
  , // rancid
  apple,
  olive
] = ['chili', 'rotten', 'rancid', 'apple', 'olive'];

// 或者

let [chili, /*rotten*/, /*rancid*/, c] = ['chili', 'rotten', 'rancid', 'keep', 'olive'];
```

## 社区案例

### 从 `split()` 的结果解析数据

解析用逗号分隔的数据，并仅获取所需数据。

_致谢：[@SamHulick](https://twitter.com/SamHulick)_

```js
const tooMuchData = '33871,LOC,type1,99.27,FN';
const [, , , price] = tooMuchData.split(',');

console.log(price); // 99.27
```

## 资源

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Ignoring_some_returned_values
- http://untangled.io/advanced-es6-destructuring-techniques/
- https://stackoverflow.com/questions/46775128/how-can-i-ignore-certain-returned-values-from-array-destructuring
- http://2ality.com/2015/01/es6-destructuring.html
