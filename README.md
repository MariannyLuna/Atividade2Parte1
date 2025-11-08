# Atividade2Parte1

##Oque é JSON? 

> JSON ou JavaScript Object Notation é uma estrutura mais leve e compacta para trocaa de dados, sendo bem mais fácil para humanos escreverem pois é baseado no padrão de linguagem de programação usando um texto legível no formato atributo-valor.
> Ele é completamente independente de linguagem, mas tem conversões para a maioria delas.

##Porque o json se tornou popular para troca de dados
entre aplicações.? 

>Pela simplicidade e compatibilidade com a maioria das linguagens de programação, sendo as principais razões:

1. Leveza
2. Legibilidade tanto para humanos quanto para máquinas
3. Estrutura Flexível
4. Uso generalizado em APIs (interfaces de programação de aplicativos)
5. Ele é independente de qualquer linguagem de programação

## Qual a diferença entre JSON.stringify() e JSON.parse()?

##JSON.stringify()
> Ele converte um objeto JS em uma string já formatada em JSON (serialização). ou seja é usado para enviar dados para uma API ou um arquivo. 

```
const pessoa = { nome: "Ana", idade: 25 };
const texto = JSON.stringify(pessoa);

console.log(texto);

// saída

{"nome":"Ana","idade":25}

```

##JSON.parse()
> Converte uma string JSON em objeto JS (desserialização). É usado quando recebemos dados em formato de texto. 
> 
```
const texto = '{"nome":"Ana","idade":25}';
const pessoa = JSON.parse(texto);

console.log(pessoa.nome);

//saída:

Ana

```
##Alguns códigos em JS com a string "JavaScript é baseada em ECMA Script" :

>Verificando se tem a palavra "script";

```

let frase = "JavaScript é baseada em ECMA Script";
let busca = "Script";

let posição = frase.indexOf(busca);

if (posição > -1) {
  console.log("Encontrei a palavra \"" + busca + "\" na frase.");
} else {
  console.log("A palavra \"" + busca + "\" não foi encontrada na frase.");
}

//saída

Encontrei a palavra "Script" na frase.

```

>Para remover a palavra "JavaScript" e gerar uma nova string;

```
let frase = "JavaScript é baseada em ECMA Script";
let busca = "JavaScript";

let posição = frase.indexOf(busca);

if (posição > -1) {
  let novaFrase = frase.slice(0, posição) + frase.slice(posição + busca.length);
  console.log("Frase sem \"" + busca + "\": " + novaFrase.trim());
} else {
  console.log("A palavra \"" + busca + "\" não foi encontrada na frase.");
}


//saída

Frase sem "JavaScript": é baseada em ECMA Script

```
>Substituir a palavra "baseada" para "tem origem";

```
let frase = "JavaScript é baseada em ECMA Script";
let busca = "baseada";
let substituta = "tem origem";

let posição = frase.indexOf(busca);

if (posição > -1) {
  let novaFrase = frase.slice(0, posição) + substituta + frase.slice(posição + busca.length);
  console.log("Frase com substituição: " + novaFrase);
} else {
  console.log("A palavra \"" + busca + "\" não foi encontrada na frase.");
}


//saída

Frase com substituição: JavaScript é tem origem em ECMA Script

```
##Qual a vantagem de usar ( ` ` ) em vez de concatenação? 

>Usar das ( ` ` ) é bem mais rápido, pratico e legivel do que usar a + da concatenação.

*Ex com concatenação:
```
const nome = "Mary";
const idade = 18;
const frase = "Meu nome é " + nome + " e eu tenho " + idade + " anos.";
console.log(frase);

//saída

Meu nome é Mary e eu tenho 18 anos.

```
*Ex com crases:

```
const nome = "Mary";
const idade = 18;
const frase = `Meu nome é ${nome} e eu tenho ${idade} anos.`;
console.log(frase);

//saída

Meu nome é Mary e eu tenho 18 anos.

```
> Resumindo, o uso de crases é bem mais vantajoso por:
1. ter uma interpolação mais limpa sem precisar juntar as partes com o +.
2. Permite um uso melhor com expressões com variáveis.
   * Ex:  const a = 5, b = 3;
console.log(`A multiplicação de ${a} e ${b} é ${a * b}`);
3. Não precisaria ter que usar \n para quebrar em linhas e concatenar varias vezes.
4. Melhor legibilidade em códigos muito grandes.

