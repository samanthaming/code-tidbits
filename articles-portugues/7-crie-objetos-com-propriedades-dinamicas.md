Translated by [@Mathias54](https://github.com/Mathias54)

# Criando Objetos Com Propriedades Dinâmicas com ES6.

A forma mais fácil de criar objetos com propriedades dinâmicas 💪

Anteriomente, nós sempre precisávamos criar uma notação de colchetes para usar propriedades dinâmicas. Com o ES6, nós finalmente podemos criar propriedades dinâmicas na declaração do objeto. Woohoo! 🤩

```javascript
var chave = '🔑';

// Forma Antiga
var cadeado = {};
cadeado[chave] = 'destravado';

// Forma Nova
var cadeado = {
  [chave]: 'destravado',
}
```