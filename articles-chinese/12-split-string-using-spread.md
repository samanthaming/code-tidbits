Translated by [@baooab](https://github.com/baooab)

# 使用 ES6 扩展运算符分割字符串

使用扩展语法可以将一个字符串转换成由字符组成的数组！

以“pizza”为例，它会遍历这个字符串中的每一个字符，并将结果赋值给新数组“splitPizza”。很酷 🤩

```javascript
const pizza = 'pizza';

// 传统方式
const slicedPizza = pizza.split('');
console.log(slicedPizza) // [ 'p', 'i', 'z', 'z', 'a' ]

// ES6: 使用扩展运算符
const slicedPizza2 = [...pizza];
console.log(slicedPizza2) // [ 'p', 'i', 'z', 'z', 'a' ]

// ES6: 使用 Array.from
const slicedPizza3 = Array.from(pizza);
console.log(slicedPizza3); // [ 'p', 'i', 'z', 'z', 'a' ]
```

## 例子

### 首字母大写

这是一个关于为什么要拆分字符串的很好的用例。

```javascript
const name = "samantha";

const capitalizeName = [
  
  // 将数组里的第一个字符格式化成大写形式
  ...name[0].toUpperCase(),
  
  // 忽略第一个字符，返回余下数组中的字符
  ...name.slice(1)
]
// 将数组成员连接成一个字符串
.join(''); 

console.log(capitalizeName); // Samantha
```

## 社区建议

### split 方法在处理 emoji 时有问题

使用扩展运算符不仅让写出的代码更加简洁，而且它还能有效处理像 emoji 这样的多字节 UTF-8 字符。

```javascript
// 使用 split 方法
"pizza🍕".split(''); // [ 'p', 'i', 'z', 'z', 'a', '�', '�' ]

// 使用扩展运算符
[..."pizza🍕"]; // [ 'p', 'i', 'z', 'z', 'a', '🍕' ]

// 使用 Array.from
Array.from("pizza🍕"); // [ 'p', 'i', 'z', 'z', 'a', '🍕' ]
```

_致谢: [@donavon](https://twitter.com/donavon/status/987764794320093185)_


### 解释 Emoji  

字符串经 split 后之所以会出现错乱的结果，是因为 '🍕' emoji 这个 emoji 的 length 值为 2。这个字符的 Unicode 码点是由一个代理对组成的。而 split 方法，会把代理对中的两个代码单元分开处理，因此会得到两个错乱的结果。

```javascript
'🍕'.length; // 2

// 披萨这个 emoji 字符由一个代理对组成（译者注：即一个字符由两个代码单元组成）
'🍕'.charCodeAt(0); // 55356
'🍕'.charCodeAt(1); // 57173

// 每个代码单元单独显示的结构是很奇怪的
String.fromCharCode(55356); // '�'
String.fromCharCode(57173); // '�'

// 但组合在一起，就能返回正确 emoji 结果了
String.fromCharCode(55356, 57173); // '🍕'
```

_致谢: Aleksandar H_

## 资源

- https://stackoverflow.com/questions/44900175/why-does-spread-syntax-convert-my-string-into-an-array
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from
- https://www.contentful.com/blog/2016/12/06/unicode-javascript-and-the-emoji-family/
- https://dmitripavlutin.com/what-every-javascript-developer-should-know-about-unicode/
- https://medium.com/@giltayar/iterating-over-emoji-characters-the-es6-way-f06e4589516
