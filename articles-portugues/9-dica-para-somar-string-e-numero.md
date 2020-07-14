Translated by [@Mathias54](https://github.com/Mathias54)

# Truque Para Somar Strings e Números.

O operador + é um atalho para converter string em números. 🤩

Problema: Somar strings que possuem números não soma eles. Invés disso, as strings são concatenadas. ❌

Solução: Converter a String para um número. Assim, poderá cálcular a soma. ✅

```javascript
const string = "100";
const numero = 5;

// Isso não retorna uma soma, retorna uma concatenação.
console.log(string + numero); // 1005

// Adiciona um "+" na string para cálcular uma soma
console.log(+string + number); // 105
```

## Referências

- [Cast to Number in Javascript using the Unary (+) Operator](https://medium.com/@nikjohn/cast-to-number-in-javascript-using-the-unary-operator-f4ca67c792ce)
