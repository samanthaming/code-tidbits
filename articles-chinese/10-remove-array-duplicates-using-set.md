Translated by [@baooab](https://github.com/baooab)

# 使用 ES6 Set 给数组去重

“Set”是一个用来存储唯一值的数据结构。不允许存储重复值。这使它成为从数组中删除重复项的理想选择，但 Set 不是数组，这就是为什么我们还要将其转为数组，这样才能使用诸如 `.map`、`.reduce` 的数组方法。


1. 使用“new Set”删除重复项
2. 使用“Array.from”将 Set 转为数组

```javascript
const duplicates = [1,2,3,4,4,1];

const uniques = Array.from(new Set(duplicates));

console.log(uniques) // [1,2,3,4,1]
```

或者使用扩展运算符将 Set 转为数组。

```javascript
const duplicates = [1,2,3,4,4,1];

const uniques = [...new Set(duplicates)];

console.log(uniques) // [1,2,3,4,1]
```
