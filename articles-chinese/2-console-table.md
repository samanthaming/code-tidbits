Translated by [@baooab](https://github.com/baooab)

# 使用 `console.table` 显示数据 

下次在开发者工具栏的 Console 面板里尝试用 `console.table` 打印数据吧，比 `console.log` 酷多了。在数组和对象上特别好用 ⭐️

```javascript
const amazingAthletes = [
  {
    firstName: "Ronda",
    lastName: "Rousey",
    sport: "🥊"
  },
  {
    firstName: "Chloe",
    lastName: "Kim",
    sport: "🏂"
  },
  {
    firstName: "Tessa",
    lastName: "Virtue",
    sport: "⛸"
  },
  {
    firstName: "Hayley",
    lastName: "Wickenheiser",
    sport: "🏒"
  }
];

console.table(amazingAthletes);
```

![Console Table](/images/2-console-table.png)
