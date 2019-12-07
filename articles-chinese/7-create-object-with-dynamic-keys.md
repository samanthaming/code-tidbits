# ES6：使用动态属性名创建对象

在之前，我们都是在方括号中设置动态属性名的。从 ES6 开始，我们终于可以在对象的字面量声明中，使用这种方式创建动态属性名了。喔！ 🤩

```javascript
var key = '🔑';

// 旧式
var lock = {};
lock[key] = 'unlock';

// 新式
var lock = {
  [key]: 'unlock';
}
```
