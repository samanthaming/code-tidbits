Translated by [@baooab](https://github.com/baooab)

# 使用解构的方式交换变量值

这次是 ES6 的解构语法起了作用 🏆

我们可以很容易的使用 ES6 解构语法交换变量值。这是修复 #奥斯卡最佳图片混搭 的好方法 😜

```javascript
let oscar = 'La La Land';
let nominee = 'Moonlight';

[oscar, nominee] = [nominee, oscar];

console.log(oscar) // Moonlight
console.log(nominee) // La La Land
```
