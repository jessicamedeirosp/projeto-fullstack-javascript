## Variáveis (são caixas que guardam valores)

- let - o valor pode ser alterado

```js
let melhorFilme = "Harry Potter";
melhorFilme = "Mentira, Jogos Vorazes";
```

- const - o valor não pode ser alterado

```js
const melhorFilme = "Jogos Vorazes";
```

### Tipos de variáveis

- string - texto

```js
const nome = "Maria";
```

- number - números

```js
const idade = 30;
```

- array - é uma caixa com divisões, onde cada parte recebe um valor

```js
const frutas = ["Maça", "Banana", "L
aranja"];
```

- object - é uma mochila, onde você pode colocar vários valores agrupados

```js
const pessoa = {
  nome: "Maria",
  idade: 30,
  gostaDeFruta: true,
  animaisDeEstimacao: ["gato", "cachorro"],
};
```

- boolean - sou true/verdadeiro ou false/falso

```js
const maiorDe18 = true;
const temCarteiraDeMotorista = false;
```

- null - vazio

```js
const nome = null; // to tão vazio
```

- undefined - não definido

```js
const nome; // to sem definição
```

## Condicionais

- if

```js
// quando a expressão do if é verdadeira é executado o que tem dentro do bloco (dentro dos colchetes), ou seja, será exibido "é igual a banana"
const fruta = "banana";
if (fruta === "banana") {
  console.log("é igual a banana");
}
```

- if e else

```js
// quando a expressão do if é falsa é executado o bloco do else, ou seja, será exibido "é diferente de banana"
const fruta = "maça";
if (fruta === "banana") {
  console.log("é igual a banana");
} else {
  console.log("é diferente de banana");
}
```

- if, else if, else

```js
// quando a expressão do if é falsa é executado o else if, se a expressão do else if for verdadeira é executado o bloco do else if, ou seja, será exibido "é igual a maça"
const fruta = "maça";
if (fruta === "banana") {
  console.log("é igual a banana");
} else if (fruta === "maça") {
  console.log("é igual a maça");
} else {
  console.log("é diferente de banana e maça");
}
```

```js
// quando da expressão do if ser falsa e a do else if ser falsa também o bloco que será executado é a do else, ou seja, será exibido "é diferente de banana e maça"
const fruta = "uva";
if (fruta === "banana") {
  console.log("é igual a banana");
} else if (fruta === "maça") {
  console.log("é igual a maça");
} else {
  console.log("é diferente de banana e maça");
}
```

## Laços de Repetição (uma fila infinida, que só acaba quando você manda)

- for

```js
const animais = ["gato", "cachorro", "papagaio"];

for (let i = 0; i < animais.length; i++) {
  console.log(animais[i]);
}
```

- for of

```js
const animais = ["gato", "cachorro", "papagaio"];

for (let item of animais) {
  console.log(item);
}
```

- while

```js
  const animais = ["gato", "cachorro", "papagaio"];

  let i = 0;

  for (i < animais.length; ) {
    console.log(animais[i]);
    i++
  }
```

## Console Vs Return

- **console.log**: exibe o conteudo no console

```js
console.log("olá Dev(a)!");
```

- **return**: retorna o contéudo

```js
return "olá Dev(a)!";
```

## Funções (é uma cafeteira - você passa algo, ela trabalha nisso e te devolve algo)

- Nomeadas

```js
function saudacao() {
  console.log("olá Dev(a)!");
}
saudacao(); // to sendo chamada
```

- Anônimas

```js
(function () {
  console.log("olá Dev(a)!");
})(); // sendo criada e chamada ao mesmo tempo (que isso bicho)
```

- Arrow Functions Nomeada

```js
const saudacao = () => {
  console.log("olá Dev(a)!");
};
saudacao();
```

- Arrow Functions Anônimas

```js
(() => {
  console.log("olá Dev(a)!");
})(); // sendo criada e chamada ao mesmo tempo (que isso bicho)
```

- Parâmetros

```js
function saudacao(nome) {
  console.log(`olá, ${nome}!`);
}
saudacao("Ana"); // to sendo chamada
```

- console

```js
function saudacao(nome) {
  console.log(`olá, ${nome}!`);
}
saudacao("Ana"); // to sendo chamada e ta exibindo Olá, Ana!
```

- return

```js
function saudacao(nome) {
  return `olá, ${nome}!`;
}
saudacao("Ana"); // to sendo chamada, mas nada está sendo exibido

const mensagem = saudacao("Lisa");
console.log(mensagem); // agora sim to sendo exibida: Olá, Lisa!

console.log(saudacao("Jess")); // desse jeito também to sendo exibida
```

## Métodos De String:

- indexOf() - index da primeira palavra

```js
const mensagem = "Eu amo minha mãe";
const indexDeMae = mensagem.indexOf("mãe"); // index 13
```

- lastIndexOf() - index da ultima palavra

```js
const mensagem = "Eu amo minha mãe. Eu amo minha mãe.";
const ultimoIndexDeMae = mensagem.lastIndexOf("mãe"); // 31
```

- includes() - verifica se inclui a palavra

```js
const mensagem = "Eu amo minha mãe";
const incluiMae = mensagem.includes("mãe"); // true
```

- slice() - quebra o texto

```js
const mensagem = "Eu amo minha mãe.";
const parteDaMensagem = mensagem.slice(0, 6); // Eu amo
```

- replace() - altera uma parte do texto

```js
const mensagem = "Eu amo minha mãe.";
const novaMensagem = mensagem.replace("amo", "amo muito"); // Eu amo muito minha mãe.
```

- toUpperCase() - deixa tudo em maiusculo

```js
const mensagem = "Eu amo minha mãe.";
const novaMensagem = mensagem.toUpperCase(); //  EU AMO MINHA MÃE.
```

- toLowerCase() - deixa tudo em minusculo

```js
const mensagem = "Eu amo minha mãe.";
const novaMensagem = mensagem.toLowerCase(); //  eu amo minha mãe.
```

- trim() - remove todos os espaços

```js
const mensagem = "   Eu amo minha mãe.   ";
const novaMensagem = mensagem.trim(); //  Eu amo minha mãe.
```

- split() - quebra o texto e cria um array

```js
const mensagem = "Eu amo minha mãe.";
const array = mensagem.split(" "); // [ 'Eu', 'amo', 'minha', 'mãe.' ]
```

- padStart() - preenche um texto no inicio

```js
const mensagem = "amo";
const novaMensagem = mensagem.padStart(20, "a"); // aaaaaaaaaaaaaaaaaamo
```

- padEnd() - preenche um texto no final

```js
const mensagem = "amo";
const novaMensagem = mensagem.padEnd(20, "0"); // amoooooooooooooooooo
```

## Métodos de Array

- length - tamanho do array

```js
const frutas = ["maça", "banana", "laranja"];
console.log(frutas.length); // 3
```

- push() - insere um elemento no fim do array

```js
const frutas = ["maça", "banana", "laranja"];
frutas.push("uva");
console.log(frutas); // ["maça", "banana", "laranja", "uva"]
```

- pop() - remove o elemento do fim do array

```js
const frutas = ["maça", "banana", "laranja"];
frutas.pop();
console.log(frutas); // ["maça", "banana"]
```

- unshift() - insere um elemento no inicio do array

```js
const frutas = ["maça", "banana", "laranja"];
frutas.unshift();
console.log(frutas); // ["uva","maça", "banana", "laranja"];
```

- shift() - remove o elemento do início do array

```js
const frutas = ["maça", "banana", "laranja"];
frutas.shift();
console.log(frutas); // ["banana", "laranja"];
```

---

- indexOf() - index (posição) da laranja

```js
const frutas = ["maça", "banana", "laranja"];
console.log(frutas.indexOf("laranja")); // 2
```

- includes() - verificar se existe o elemento no array

```js
const frutas = ["maça", "banana", "laranja"];
console.log(frutas.includes("laranja")); // true
```

- concat() - junta dois arrays

```js
const frutasAmarelas = ["mexerica", "laranja"];
const frutasVermelhas = ["maça", "amora"];
const frutas = frutasAmarelas.concat(frutasVermelhas);
console.log(frutas); // [ 'mexerica', 'laranja', 'maça', 'amora' ]
```

- splice() - altera o contéudo da lista

```js
const meses = ["Jan", "Mar", "Abr", "Jun"];
meses.join();
console.log(meses); // [ 'Jan', 'Fev', 'Mar', 'Abr', 'Jun' ]
```

- join()

```js
const meses = ["Jan", "Mar", "Abr", "Jun"];
console.log(meses.join()); // Jan, Mar, Abr, Jun;
```

- reverse() - inverte array

```js
const meses = ["Jan", "Mar", "Abr", "Jun"];
console.log(meses.reverse()); // [ 'Jun', 'Abr', 'Mar', 'Jan' ]
```

- slice() - quebra o array

```js
const meses = ["Jan", "Mar", "Abr", "Jun"];
console.log(meses.slice(1, 2)); // [ 'Mar' ]
```

- toString() - transforma em string

```js
const meses = ["Jan", "Mar", "Abr", "Jun"];
console.log(meses.toString()); // Jan,Mar,Abr,Jun
```

---

- every() - verifica se todos os elementos passam nos testes da função fornecida

```js
const animais = ["gato", "pato", "cachorro"];
console.log(animais.every((item) => item == "gato")); // false
```

- some() - verifica se ao menos um dos elementos passam nos testes da função fornecida

```js
const animais = ["gato", "pato", "cachorro"];
console.log(animais.some((item) => item == "gato")); // true
```

- find() - traz o primeiro elemento que passam nos testes da função fornecida

```js
const animais = ["gato", "pato", "cachorro"];
console.log(animais.find((item) => item !== "gato")); // pato
```

- findIndex() - traz o index (posição) do primeiro elemento que passam nos testes da função fornecida

```js
const animais = ["gato", "pato", "cachorro"];
console.log(animais.findIndex((item) => item !== "gato")); // 1
```

- filter() - traz um novo array com os elementos que passam nos testes da função fornecida

```js
const numeros = [1, 2, 3, 4, 5];
console.log(numeros.filter((item) => item !== 2)); // [ 1, 3, 4, 5 ]
```

- map() - array com a mesma qtd de elementos do array original

```js
const numeros = [1, 2, 3, 4, 5];
console.log(numeros.map((item) => item * 2)); // [ 2, 4, 6, 8, 10 ]
```

---

- sort() - ordena os elementos

```js
const numeros = [8, 20, 3, 4, 9];
console.log(numeros.sort((a, b) => a - b)); // [ 3, 4, 8, 9, 20 ]

console.log(numeros.sort((a, b) => b - a)); // [ 20, 9, 8, 4, 3 ]
```

- reduce() - executa uma função para reduzir um array em um único valor

```js
const numeros = [8, 20, 3, 4, 9];
console.log(numeros.reduce((acc, x) => (acc += x), 0)); // 44
```
