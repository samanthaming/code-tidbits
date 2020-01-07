Translated by [@Mathias54](https://github.com/Mathias54)

# Trocando Valores de Variáveis com o Destructor

ES6 Destructor para o resgate 🏆

O método mais fácil de trocar o valor de duas variáveis é usando o Destructor do ES6. Essa é uma ótima forma de corrigir a premiação de Oscar para Melhor Filme.  

```javascript
let oscar = 'La La Land';
let nomeado = 'Moonlight';

[oscar, nomeado] = [nomeado, oscar];

console.log(oscar); // Moonlight
console.log(nomeado); // La La Land
```
