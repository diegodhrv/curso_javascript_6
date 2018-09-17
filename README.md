# Curso de Javascript 6

## [1. **Fundamentos**](#1-fundamentos-1)
- [**O Básico de Var, Let e Const**](#o-básico-de-var-let-e-const)
- [**Tipagem Fraca**](#tipagem-fraca)
- [**Tipos em Javascript - Number**](#tipos-em-javascript---number)
- [**Tipos em Javascript - String**](#tipos-em-javascript---string)
- [**Tipos em Javascript - Boolean**](#tipos-em-javascript---boolean)
- [**Tipos em Javascript - Array**](#tipos-em-javascript---array)
- [**Tipos em Javascript - Object**](#tipos-em-javascript---object)
- [**Entendendo o Null & Undefined**](#entendendo-o-null--undefined)
- [**Básico de Funções**](#básico-de-funções)
- [**Usando Var e Let**](#usando-var-e-let)
- [**Entendendo o Hoisting**](#entendendo-o-hoisting)
- [**Função vs Objeto**](#função-vs-objeto)
- [**Par Nome Valor**](#par-nome-valor)
- [**Notação Ponto**](#notação-ponto)
- [**Operadores - Atribuição**](#operadores-atribuição)
- [**Operadores - Destructing**](#operadores-destructuring)
- [**Operadores - Aritmeticos**](#operadores-aritmeticos)
- [**Operadores - Relacionais**](#operadores-relacionais)
- [**Operadores - Lógicos**](#operadores-lógicos)
- [**Operadores - Unário**](#operadores-unário)
- [**Operadores - Ternário**](#operadores-ternário)
- [**Operador: Rest/Spread**](#operador-restspread)
- [**Tratamento de Erro Try/Catch/Throw**](#tratamento-de-erro-trycatchthrow)
## [2. **Estrutura de Controle**](#2-estrutura-de-controle-1)
- [**Usando a estrutura IF**](#usando-a-estrutura-if)
- [**Usando a estrutura IF/ELSE**](#usando-a-estrutura-ifelse)
- [**Usando a estrutura IF/ELSE/IF**](#usando-a-estrutura-ifelseif)
- [**Usando a estrutura SWITCH**](#usando-a-estrutura-switch)
- [**Usando a estrutura WHILE**](#usando-a-estrutura-while)
- [**Usando a estrutura DO/WHILE**](#usando-a-estrutura-dowhile)
- [**Usando a estrutura FOR**](#usando-a-estrutura-for)
- [**Usando a estrutura FOR/IN**](#usando-a-estrutura-forin)
- [**Usando a estrutura Break/Continue**](#usando-a-estrutura-breakcontinue)
## [3. **Função**](#3-função-1)
- [**Cidadão de Primeira Linha**](#cidadão-de-primeira-linha)
- [**Parâmetros e Retorno São Opcionais**](#parâmetros-e-retorno-são-opcionais)
- [**Parâmetros Variáveis**](#parâmetros-varáveis)
- [**Parâmetro Padrão**](#parâmetro-padrão)
- [**"this" Pode Variar**](#this-pode-variar)
- [**"this" e a Função Bind**](#this-e-a-função-bind)
- [**Funções Arrow**](#funções-arrow)
- [**Funções Anônimas**](#funções-anônimas)
- [**Funções Callback**](#funções-callback)
- [**Funções Construtoras:**](#funções-construtoras)
- [**Tipos de Declaração:**](#tipos-de-declaração)
- [**Contexto Léxico:**](#contexto-léxico)
- [**Closures:**](#closures)
- [**Função Factory:**](#função-fectory)
- [**Class vs Factory:**](#class-vs-factory)
- [**IIFE:**](#iife)
- [**Call e Apply:**](#call-e-apply)
## [4. **Objetos**](#4-objeto)
- [**Criar Objetos**](#criar-objetos)
- [**Objetos Constatntes**](#objetos-constantes)
- [**Notação Literal (criando atributos no objeto)**](#notação-literal-criando-atributos-no-objeto)
- [**Getters e Setters**](#getters-e-setters)
- [**Funções Importantes de Objeto**](#funções-importantes-de-objeto)
- [**Herança**](#herança)
- [**Evitando Modificações**](#evitando-modificações)
- [**Json vs Objeto**](#json-vs-objeto)
- [**Classe**](#classe)
## [5. **Array**](#5-array-1)
- [**Visão Geral**](#visão-geral)
- [**Métodos Importantes**](#métodos-importantes)
- [**Simulando Array com Objeto**](#simulando-array-com-objeto)
- [**Foreach**](#foreach)
- [**Map**](#map)
- [**Filter**](#filter)
- [**Reduce**](#reduce)
- [**Concat**](#concat)
- [**FlatMap**](#flatmap)

## 1. **Fundamentos**

### **O Básico de Var, Let e Const:**

>Dados e estrutura de dados. De forma geral, usar o Let para declarar variáveis
```javascript
var a = 3
let b = 4

var a = 30 //Var permite que a variavel seja redeclarada
b = 40

console.log(a, b)

a = 300
b = 400

console.log(a, b)

const c = 5
// c = 50
console.log(c)
```
[Topo](#curso-de-javascript-6)

### **Tipagem Fraca:**

>Uma linguagem de tipagem dinâmica
```javascript
let qualquer = 'Legal'
console.log(qualquer)
console.log(typeof qualquer)

qualquer = 3.1516
console.log(qualquer)
console.log(typeof qualquer)

// Evitar nome genéricos e siglas
let valor = ''
let numero = 1
let pqp = false // Produto Químico Perigoso... kkk
```
[Topo](#curso-de-javascript-6)

### **Tipos em Javascript - Number:**

>Função Number
```javascript
const peso1 = 1.0
const peso2 = Number('2.0')//Tenta converter para Number

console.log(peso1, peso2)
console.log(Number.isInteger(peso1))//Saber se é um valor inteiro
console.log(Number.isInteger(peso2))

const avaliacao1 = 9.871
const avaliacao2 = 6.871

const total = avaliacao1 * peso1 + avaliacao2 * peso2
const media = total / (peso1 + peso2)

console.log(media.toFixed(2))//Limitar a quantidade de casas decimais
console.log(media.toString(2)) // em binário
console.log(typeof media)
console.log(typeof Number)
```
[Topo](#curso-de-javascript-6)

>Number:Alguns Cuidados
```javascript
console.log(7 / 0)//Retorna Infinity
console.log("10" / 2)//Retorna 5
console.log('3' + 2) // string ganha!
console.log('3' - 2)
console.log("Show!" * 2)//Retorna NaN(Not a Number)
console.log(0.1 + 0.7)
// console.log(10.toString())
console.log((10.345).toFixed(2))
```
[Topo](#curso-de-javascript-6)

>Usando o Math
```javascript
const raio = 5.6
const area = Math.PI * Math.pow(raio, 2)//Raio elevado ao quadrado

console.log(area)
console.log(typeof Math)
```
[Topo](#curso-de-javascript-6)

### **Tipos em Javascript - String:**

>String é uma cadeia de caracteres delimitada por aspas simples ou duplas 
```javascript
const escola = "Cod3r"

console.log(escola.charAt(4))//Retorna a letra que está dentro do indice 4 da strintg
console.log(escola.charAt(5))
console.log(escola.charCodeAt(3))//Retorna o valor dele da tabela ASCII
console.log(escola.indexOf('3'))

console.log(escola.substring(1))//Retorna uma string a partir do indice 1
console.log(escola.substring(0, 3))

console.log('Escola '.concat(escola).concat("!"))
console.log('Escola ' + escola + "!")
console.log(escola.replace(3, 'e'))//O segundo parametro aceita expressão regular

console.log('Ana,Maria,Pedro'.split(','))//Retorna um array quebrado por virgula 
```
[Topo](#curso-de-javascript-6)

>Usando Template String
````javascript
const nome = 'Rebeca'
const concatenacao = 'Olá ' + nome + '!'
const template = `
    Olá
    ${nome}!`
console.log(concatenacao, template)

// expressoes...
console.log(`1 + 1 = ${1 + 1}`)

const up = texto => texto.toUpperCase()
console.log(`Ei... ${up('cuidado')}!`)
````
[Topo](#curso-de-javascript-6)

### **Tipos em Javascript - Boolean:**
>Tipos de Boolean em javascript. Todos os numeros são verdadeiros, menos o zero.  
```javascript
let isAtivo = false
console.log(isAtivo)

isAtivo = true
console.log(isAtivo)

isAtivo = 1//1 tbm é um boolean em javascript
console.log(!!isAtivo)

console.log('os verdadeiros...')
console.log(!!3)
console.log(!!-1)
console.log(!!' ')
console.log(!!'texto')
console.log(!![])
console.log(!!{})
console.log(!!Infinity)
console.log(!!(isAtivo = true))

console.log('os falsos...')
console.log(!!0)
console.log(!!'')
console.log(!!null)
console.log(!!NaN)
console.log(!!undefined)
console.log(!!(isAtivo = false))

console.log('pra finalizar...')
console.log(!!('' || null || 0 || ' '))//Ele retorna o valor verdadeiro 

let nome = 'Lucas'
console.log(nome || 'Desconhecido')//Ele retorna o valor verdadeiro. Usar o operdaor OU para retornar um valor verdadeiro
```
[Topo](#curso-de-javascript-6)

### **Tipos em Javascript - Array:**
>Array em javascript. Todo Array em javascript é um objeto 
```javascript
const valores = [7.7, 8.9, 6.3, 9.2]
console.log(valores[0], valores[3])
console.log(valores[4])

valores[4] = 10
console.log(valores)
console.log(valores.length)

valores.push({id: 3}, false, null, 'teste')
console.log(valores)

console.log(valores.pop())
delete valores[0]
console.log(valores)

console.log(typeof valores)
```
[Topo](#curso-de-javascript-6)

### **Tipos em Javascript - Object:**
> 
```javascript
const prod1 = {}
prod1.nome = 'Celular Ultra Mega'
prod1.preco = 4998.90
prod1['Desconto Legal'] = 0.40 // evitar atributos com espaço

console.log(prod1)

const prod2 = {
    nome: 'Camisa Polo',
    preco: 79.90
}

console.log(prod2)
```
[Topo](#curso-de-javascript-6)

### **Entendendo o Null & Undefined**
>Undefined é quando a variavel é declarada, mas não é inicializada. Null é quando a variavel não tem nenhuma referencia, não aponta pra nenhum endereço de memória, então a variavel referencia é definida com o valor null, neste caso. Ou se não tem nenhum valor primitivo atribuida a ela, mas sim null, lembrando que Null é um valor.
```javascript
let valor // não inicializada
console.log(valor)

valor = null // ausência de valor
console.log(valor)
// console.log(valor.toString()) // Erro!

const produto = {}
console.log(produto.preco)
console.log(produto)

produto.preco = 3.50
console.log(produto)

produto.preco = undefined // evite atribuir undefined
console.log(!!produto.preco)
// delete produto.preco
console.log(produto)

produto.preco = null // sem preço
console.log(!!produto.preco)
console.log(produto)
```
[Topo](#curso-de-javascript-6)

### **Básico de funções**
>
````javascript
// Funcao sem retorno
function imprimirSoma(a, b) {
    console.log(a + b)
}

imprimirSoma(2, 3)
imprimirSoma(2)
imprimirSoma(2, 10, 4, 5, 6, 7, 8)
imprimirSoma()

// Funcao com retorno
function soma(a, b = 1) {//O parametro b recebe um 1 como valor padrao se nada for passado a ele
    return a + b
}

console.log(soma(2, 3))
console.log(soma(2))
console.log(soma())
````
[Topo](#curso-de-javascript-6)

>Mais de funções. Atribuindo funções a uma variavel
````javascript
// Armazenando uma funcao em uma variavel
const imprimirSoma = function (a, b) {
    console.log(a + b)
}

imprimirSoma(2, 3)

// Armazenando uma funcao arrow em uma variavel
const soma = (a, b) => {
    return a + b
}

console.log(soma(2, 3))

// retorno implícito
const subtracao = (a, b) => a - b
console.log(subtracao(2, 3))

const imprimir2 = a => console.log(a)
imprimir2('Legal!!!')
````
[Topo](#curso-de-javascript-6)

### **Usando Var e Let:**
>Var tem escopo de função e não de bloco. Já o Let tem escopo de bloco por esse motivo é mais utilizada
````javascript
{ 
    { 
        { 
            { 
                var sera = 'Será???'
                console.log(sera)
            }
        }
    }
}

console.log(sera)

function teste() {
    var local = 123
    console.log(local)
}

teste()
console.log(local)
````
[Topo](#curso-de-javascript-6)

>Como explicado, Var não tem escopo de bloco, mas sim escopo de função e global
````javascript
var numero = 1
{
    var numero = 2
    console.log('dentro =', numero)
}
console.log('fora =', numero)
````
[Topo](#curso-de-javascript-6)

>Let tem escopo global, escopo de função e escopo de bloco
````javascript
let numero = 1
{
    let numero = 2
    console.log('dentro =', numero)
}
console.log('fora =', numero)
````
[Topo](#curso-de-javascript-6)

>Usando Var em Loop. A variavel pode ser usada fora do Loop se ela for declarada com Var, pois Var não tem escopo de bloco
````javascript
for (var i = 0; i < 10; i++) {
    console.log(i)
}

console.log('i =', i)
````
[Topo](#curso-de-javascript-6)

>Usando Var em Loop.
````javascript
const funcs = []

for (var i = 0; i < 10; i++) {
    funcs.push(function() {
        console.log(i)
    })
}

funcs[2]()
funcs[8]()
````
[Topo](#curso-de-javascript-6)

>Usando Let em Loop. A variavel não estará visivel fora do bloco, pois Let tem escopo de bloco
````javascript
for (let i = 0; i < 10; i++) {
    console.log(i)
}

console.log('i =', i)
````
[Topo](#curso-de-javascript-6)

>Usando Let em Loop.
````javascript
const funcs = []

for (let i = 0; i < 10; i++) {
    funcs.push(function() {
        console.log(i)
    })
}

funcs[2]()
funcs[6]()
funcs[8]()
````
[Topo](#curso-de-javascript-6)

## **Entendendo o Hoisting:**
>Mover a declaração para o topo. Com Let não acontece Hoisting

````javascript
console.log('a =', a)
var a = 2
console.log('a =', a)

console.log('b =', b)
let b = 2
console.log('b =', b)
````
[Topo](#curso-de-javascript-6)

## **Função vs Objeto:**
>

````javascript
console.log(typeof Object)
console.log(typeof new Object)

const Cliente = function() {}
console.log(typeof Cliente)
console.log(typeof new Cliente)

class Produto {} // ES 2015 (ES6)
console.log(typeof Produto)
console.log(typeof new Produto())
````
[Topo](#curso-de-javascript-6)

## **Par Nome Valor:**
>

````javascript
// par nome/valor
const saudacao = 'Opa' // contexto léxico 1

function exec() {
    const saudacao = 'Falaaa' // contexto léxico 2
    return saudacao
}

// Objetos são grupos aninhados de pares nome/valor
const cliente = {
    nome: 'Pedro',
    idade: 32,
    peso: 90,
    endereco: {
        logradouro: 'Rua Muito Legal',
        numero: 123
    }
}

console.log(saudacao)
console.log(exec())
console.log(cliente)
````

## **Notação Ponto:**
>

````javascript
console.log(Math.ceil(6.1))

const obj1 = {}
obj1.nome = 'Bola'
// obj1['nome'] = 'Bola2'
console.log(obj1.nome)

function Obj(nome) {
    this.nome = nome
    this.exec = function() {
        console.log('Exec...')
    }
}

const obj2 = new Obj('Cadeira')
const obj3 = new Obj('Mesa')
console.log(obj2.nome)
console.log(obj3.nome)
obj3.exec()
````
[Topo](#curso-de-javascript-6)

## **Operadores: Atribuição**
>

````javascript
const a = 7
let b = 3

b += a // b = b + a
console.log(b)

b -= 4 // b = b - 4
console.log(b)

b *= 2 // b = b * 2
console.log(b)

b /= 2 // b = b / 2
console.log(b)

b %= 2 // b = b % 2
console.log(b)
````
[Topo](#curso-de-javascript-6)

## **Operadores: Destructuring**
>Primeira explicação. Operador de desestruturação, extração de atributos. Extração de valores para a criação de uma variavel

````javascript
// novo recurso do ES2015

const pessoa = {
    nome: 'Ana',
    idade: 5,
    endereco: {
        logradouro: 'Rua ABC',
        numero: 1000
    }
}

const { nome, idade } = pessoa //Está tirando de dentro do objeto pessoa os atributos nome e idade
console.log(nome, idade)

const { nome: n, idade: i } = pessoa //Está tirando de dentro do objeto pessoa os atributos nome e idade, e atribuindo seus valores
console.log(n, i)                    //para as variaveis n e i

const { sobrenome, bemHumorada = true } = pessoa //Retirar atributos que não existem dentro do objeto
console.log(sobrenome, bemHumorada)

const { endereco: { logradouro, numero, cep } } = pessoa
console.log(logradouro, numero, cep)

const { conta: { ag, num } } = pessoa
console.log(ag, num)
````
[Topo](#curso-de-javascript-6)

>Segunda explicação. Desestruturação de um array

````javascript
const [a] = [10]
console.log(a)

const [n1, , n3, , n5, n6 = 0] = [10, 7, 9, 8]//Extraindo valores de um array para a criação de variaveis 
console.log(n1, n3, n5, n6)

const [, [, nota]] = [[, 8, 8], [9, 6, 8]]
console.log(nota)
````
[Topo](#curso-de-javascript-6)

>Terceira explicação. Desestruturação na passagem de parametros

````javascript
function rand({ min = 0, max = 1000 }) {
    const valor = Math.random() * (max - min) + min
    return Math.floor(valor)
}

const obj = { max: 50, min: 40 }
console.log(rand(obj))
console.log(rand({ min: 955 }))
console.log(rand({}))
console.log(rand())
````
[Topo](#curso-de-javascript-6)

>Quarta explicação. Desestruturação na passagem de parametros com array

````javascript
function rand([min = 0, max = 1000]) {
    if (min > max) [min, max] = [max, min]
    const valor = Math.random() * (max - min) + min
    return Math.floor(valor)
}

console.log(rand([50, 40]))
console.log(rand([992]))
console.log(rand([, 10]))
console.log(rand([]))
console.log(rand())
````
[Topo](#curso-de-javascript-6)

## **Operadores: Aritmeticos**
>
````javascript
const [a, b, c, d] = [3, 5, 1, 15]

const soma = a + b + c + d
const subtracao = d - b
const multiplicacao = a * b
const divisao = d / a
const modulo = a % 2

console.log(soma, subtracao, multiplicacao, -divisao, modulo)
````
[Topo](#curso-de-javascript-6)

## **Operadores: Relacionais**
>Verdadeiro ou Falso. Ele compara valor e tipo, pois alguns só compara valor e outros compara valor e tipo
````javascript
console.log('01)', '1' == 1)
console.log('02)', '1' === 1)// estritamente igual
console.log('03)', '3' != 3)
console.log('04)', '3' !== 3)

console.log('05)', 3 < 2)
console.log('06)', 3 > 2)
console.log('07)', 3 <= 2)
console.log('08)', 3 >= 2)

const d1 = new Date(0)
const d2 = new Date(0)
console.log('09)', d1 === d2)
console.log('10)', d1 == d2)
console.log('11)', d1.getTime() === d2.getTime())

console.log('12)', undefined == null)
console.log('13)', undefined === null)
````
[Topo](#curso-de-javascript-6)

## **Operadores: Lógicos**
>
````javascript
function compras(trabalho1, trabalho2) {
    const comprarSorvete = trabalho1 || trabalho2
    const comprarTv50 = trabalho1 && trabalho2
    // const comprarTv32 = !!(trabalho1 ^ trabalho2) // bitwise xor
    const comprarTv32 = trabalho1 != trabalho2
    const manterSaudavel = !comprarSorvete // operador unário

    return { comprarSorvete, comprarTv50, comprarTv32, manterSaudavel }
}

console.log(compras(true, true))
console.log(compras(true, false))
console.log(compras(false, true))
console.log(compras(false, false))
````
[Topo](#curso-de-javascript-6)

## **Operadores: Unário**
>A forma pré-fixada tem precedencia sobre a forma pós-fixada 
````javascript
let num1 = 1
let num2 = 2

num1++
console.log(num1)
--num1
console.log(num1)

console.log(++num1 === num2--)
console.log(num1 === num2)
````
[Topo](#curso-de-javascript-6)

## **Operadores: Ternário**
>
````javascript
const resultado = nota => nota >= 7 ? 'Aprovado' : 'Reprovado'

console.log(resultado(7.1))
console.log(resultado(6.7))
````
[Topo](#curso-de-javascript-6)

## **Operador: Rest/Spread**
>
````javascript
// operador ... rest(juntar)/spread(espalhar)
// usar rest com parâmetro de função

// operador rest
function total(...numeros) {
    let total = 0
    numeros.forEach(n => total += n)
    return total
}
console.log(total(2, 3, 4, 5))

// usar spread com objeto
const funcionario = { nome: 'Maria', salario: 12348.99 }
const clone = { ativo: true, ...funcionario }
console.log(clone)

// usar spread com array
const grupoA = ['João', 'Pedro', 'Gloria']
const grupoFinal = ['Maria', ...grupoA, 'Rafaela']
console.log(grupoFinal)
````
[Topo](#curso-de-javascript-6)

## **Tratamento de Erro Try/Catch/Throw**
>Tratar exceções de erro lançadas pelas linhas de sentença
````javascript
function tratarErroELancar(erro) {
    // throw new Error('...')
    // throw 10
    // throw true
    // throw 'mensagem'
    throw {
        nome: erro.name,
        msg: erro.message,
        date: new Date
    }
}

function imprimirNomeGritado(obj) {
    try {
        console.log(obj.name.toUpperCase() + '!!!')
    } catch (e) {
        tratarErroELancar(e)
    } finally {             //O finally é executado logo em seguida do Try ou do Catch
        console.log('final')
    }
}

const obj = { nome: 'Roberto' }
imprimirNomeGritado(obj)
````
[Topo](#curso-de-javascript-6)

## 2. **Estrutura de controle**

### **Usando a estrutura IF**
>
````javascript
function soBoaNoticia(nota) {
    if(nota >= 7) {
        console.log('Aprovado com ' + nota)
    }
}

soBoaNoticia(8.1)
soBoaNoticia(6.1)

function seForVerdadeEuFalo(valor) {
    if(valor) {
        console.log('É verdade... ' + valor)
    }
}

seForVerdadeEuFalo()
seForVerdadeEuFalo(null)
seForVerdadeEuFalo(undefined)
seForVerdadeEuFalo(NaN)
seForVerdadeEuFalo('')
seForVerdadeEuFalo(0)
seForVerdadeEuFalo(-1)
seForVerdadeEuFalo(' ')
seForVerdadeEuFalo('?')
seForVerdadeEuFalo([])
seForVerdadeEuFalo([1, 2])
seForVerdadeEuFalo({})
````
>Um ponto e virgula seguido do if é uma sentença vazia
````javascript
function teste1(num) {
    if(num > 7)
        console.log(num)
    
    console.log('Final')
}

teste1(6)
teste1(8)

function teste2(num) {
    if(num > 7); { // cuidado com o ';', não usar com as estruturas de controle
        console.log(num)
    }
}

teste2(6)
teste2(8)
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura IF/ELSE**
>
````javascript
const imprimirResultado = function(nota) {
    if(nota >= 7) {
        console.log('Aprovado!')
    } else {
        console.log('Reprovado!')
    }
}

imprimirResultado(10)
imprimirResultado(4)
imprimirResultado('Epa!') // cuidado!!!
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura IF/ELSE/IF**
>
````javascript
Number.prototype.entre = function (inicio, fim) {
    return this >= inicio && this <= fim
}

const imprimirResultado = function (nota) {
    if (nota.entre(9, 10)) {
        console.log('Quadro de Honra')
    } else if(nota.entre(7, 8.99)) {
        console.log('Aprovado')
    } else if(nota.entre(4, 6.99)) {
        console.log('Recuperação')
    } else if(nota.entre(0, 3.99)) {
        console.log('Reprovado')
    } else {
        console.log('Nota inválida')
    }
}

imprimirResultado(10)
imprimirResultado(8.9)
imprimirResultado(6.55)
imprimirResultado(2.3)
imprimirResultado(-1)
imprimirResultado(11)
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura SWITCH**
>
````javascript
const imprimirResultado = function (nota) {
    switch (Math.floor(nota)) {
        case 10:
        case 9:
            console.log('Quadro de Honra')
            break
        case 8: case 7:
            console.log('Aprovado')
            break
        case 6: case 5: case 4:
            console.log('Recuperação')
            break
        case 3: case 2: case 1: case 0:
            console.log('Reprovado')
            break
        default:
            console.log('Nota inválida')
    }
}

imprimirResultado(10)
imprimirResultado(8.9)
imprimirResultado(6.55)
imprimirResultado(2.3)
imprimirResultado(-1)
imprimirResultado(11)
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura WHILE**
>
````javascript
function getInteiroAleatorioEntre(min, max) {
    const valor = Math.random() * (max - min) + min
    return Math.floor(valor)
}

let opcao = 0

while (opcao != -1) {
    opcao = getInteiroAleatorioEntre(-1, 10)
    console.log(`Opção escolhida foi ${opcao}.`)
}

console.log('Até a próxima!')
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura DO/WHILE**
>
````javascript
function getInteiroAleatorioEntre(min, max) {
    const valor = Math.random() * (max - min) + min
    return Math.floor(valor)
}

let opcao = -1

do {
    opcao = getInteiroAleatorioEntre(-1, 10)
    console.log(`Opção escolhida foi ${opcao}.`)
} while (opcao != -1)

console.log('Até a próxima!')
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura FOR**
>
````javascript
let contador = 1
while(contador <= 10) {
    console.log(`contador = ${contador}`)
    contador++
}

for(let i = 1; i <= 10; i++) {
    console.log(`i = ${i}`)
}

const notas = [6.7, 7.4, 9.8, 8.1, 7.7]
for(let i = 0; i < notas.length; i++) {
    console.log(`nota = ${notas[i]}`)
}
````
[Topo](#curso-de-javascript-6)

### **Usando a Estrutura FOR/IN**
>Ele passa o indice para a variavel i
````javascript
const notas = [6.7, 7.4, 9.8, 8.1, 7.7]

for (let i in notas) {
    console.log(i, notas[i])
}

const pessoa = {
    nome: 'Ana',
    sobrenome: 'Silva',
    idade: 29,
    peso: 64
}

for(let atributo in pessoa) {
    console.log(`${atributo} = ${pessoa[atributo]}`)
}
````
[Topo](#curso-de-javascript-6)

### **Usando Break/Continue**
>O break pula estrutura de controle, como FOR, WHILE, DO/WHILE... Já o continue interronpe a execução da estrtura voltando para o inicio, ele não sai da estrutura de controle
````javascript
const nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for (x in nums) {
    if (x == 5) {
        break
    }
    console.log(`${x} = ${nums[x]}`)
}

for (y in nums) {
    if (y == 5) {
        continue
    }
    console.log(`${y} = ${nums[y]}`)
}

externo:
for (a in nums) {
    for (b in nums) {
        if(a == 2 && b == 3) break externo
        console.log(`Par = ${a},${b}`)
    }
}
````
[Topo](#curso-de-javascript-6)

## 3. **Função**

### **Cidadão de Primeira Linha:**
>As funções em javascript podem ser armazenadas em variaveis, passadas por parametro, criar função dentro de outra, criar função dentro de um array, criar função dentro de um objeto e retornar função
````javascript
// Função em JS é First-Class Object (Citizens)
// Higher-order function

// criar de forma literal
function fun1() { }

// Armazenar em uma variável. para invocar a função tem que ser com os parenteses, nome da variavel seguida de parenteses. S
// Só não é necessario parenteses se ela for passada por parametro
const fun2 = function () { }

// Armazenar em um array
const array = [function (a, b) { return a + b }, fun1, fun2]
console.log(array[0](2, 3))

// Armazenar em um atributo de objeto
const obj = {}
obj.falar = function () { return 'Opa' }
console.log(obj.falar())

// Passar função como param
function run(fun) {
    fun()
}

run(function () { console.log('Executando...') })

// Um função pode retornar/conter um função
function soma(a, b) {
    return function (c) {
        console.log(a + b + c)
    }
}

soma(2, 3)(4)
const cincoMais = soma(2, 3)
cincoMais(4)
````
[Topo](#curso-de-javascript-6)

### **Parâmetros e Retorno São Opcionais:**
>
````javascript
function area(largura, altura) {
    const area = largura * altura
    if (area > 20) {
        console.log(`Valor acima do permitido: ${area}m2.`)
    } else {
        return area
    }
}

console.log(area(2, 2))
console.log(area(2))
console.log(area())
console.log(area(2, 3, 17, 22, 44))
console.log(area(5, 5))
````
[Topo](#curso-de-javascript-6)

### **Parâmetros Variáveis:**
>Arguments é um array interno de uma função que recebe todos os argumentos passados por parametro 
````javascript
function soma() {
    let soma = 0
    for (i in arguments) {
        soma += arguments[i]
    }
    return soma
}

console.log(soma())
console.log(soma(1))
console.log(soma(1.1, 2.2, 3.3))

console.log(soma(1.1, 2.2, "Teste"))
console.log(soma('a', 'b', 'c'))
````
[Topo](#curso-de-javascript-6)

### **Parâmetro Padrão:**
>
````javascript
// estrategia 1 para gerar valor padrão
function soma1(a, b, c) {
    a = a || 1
    b = b || 1
    c = c || 1
    return a + b + c
}

console.log(soma1(), soma1(3), soma1(1, 2, 3), soma1(0, 0, 0))

// estrategia 2, 3 e 4 para gerar valor padrão
function soma2(a, b, c) {
    a = a !== undefined ? a : 1
    b = 1 in arguments ? b : 1
    c = isNaN(c) ? 1 : c
    return a + b + c
}

console.log(soma2(), soma2(3), soma2(1, 2, 3), soma2(0, 0, 0))

// valor padrão do es2015
function soma3(a = 1, b = 1, c = 1) {
    return a + b + c
}

console.log(soma3(), soma3(3), soma3(1, 2, 3), soma3(0, 0, 0))
````
[Topo](#curso-de-javascript-6)

### **"this" Pode Variar:**
>Usar sempre Arrow function quando for usar o this, pois ele não irá variar de acordo com o contexto.
````javascript
````
[Topo](#curso-de-javascript-6)

### **"this" e a Função Bind:**
>Primeira explicação. Bind é utilizado para manter o this dentro de um contexto
````javascript
const pessoa = {
    saudacao: 'Bom dia!',
    falar() {
        console.log(this.saudacao)
    }
}

pessoa.falar()
const falar = pessoa.falar
falar() // conflito entre paradigmas: funcional e OO

const falarDePessoa = pessoa.falar.bind(pessoa)
falarDePessoa()
````
[Topo](#curso-de-javascript-6)

>Segunda explicação.
````javascript
function Pessoa() {
    this.idade = 0

    const self = this
    setInterval(function() {
        self.idade++
        console.log(self.idade)
    }/*.bind(this)*/, 1000)
}

new Pessoa
````
[Topo](#curso-de-javascript-6)

### **Funções Arrow:**
>Primeira explicação. Função Arrow é sempre uma função anonima, se quiser utiliza-la tem que atribuir em uma variavel. E se tiver uma unica linha de sentença e não for usada as chaves o retorno é implicito
````javascript
let dobro = function (a) {
    return 2 * a
}

dobro = (a) => {
    return 2 * a 
}

dobro = a => 2 * a // return implícito
console.log(dobro(Math.PI))

let ola = function () {
    return 'Olá'
}

ola = () => 'Olá'
ola = _ => 'Olá' // possui um param
console.log(ola())
````
[Topo](#curso-de-javascript-6)

>Segunda explicação. Usando função arrow para sempre manter o contexto do this
````javascript
function Pessoa() {
    this.idade = 0

    setInterval(() => {
        this.idade++
        console.log(this.idade)
    }, 1000)
}

new Pessoa
````
[Topo](#curso-de-javascript-6)

>Terceira explicação. Usando arrow function o this aponta para o objeto no qual a função foi escrita. Então o correto, para evitar problemas é usar o this em arrow function. O this utilizado em uma arrow function não varia de forma alguma, ela sempre fira presa ao ontexto que foi escrita, ou seja, associada ao objeto que foi escrita.
````javascript
let comparaComThis = function (param) {
    console.log(this === param)
}

comparaComThis(global)

const obj = {}
comparaComThis = comparaComThis.bind(obj)
comparaComThis(global)
comparaComThis(obj)

let comparaComThisArrow = param => console.log(this === param)
comparaComThisArrow(global)
comparaComThisArrow(module.exports)

comparaComThisArrow = comparaComThisArrow.bind(obj)
comparaComThisArrow(obj)
comparaComThisArrow(module.exports)
````
[Topo](#curso-de-javascript-6)

### **Funções Anônimas:**
>
````javascript
const soma = function (x, y) {
    return x + y
}

const imprimirResultado = function (a, b, operacao = soma) {
    console.log(operacao(a, b))
}

imprimirResultado(3, 4)
imprimirResultado(3, 4, soma)
imprimirResultado(3, 4, function (x, y) {
    return x - y
})
imprimirResultado(3, 4, (x, y) => x * y)

const pessoa = {
    falar: function () {
        console.log('Opa')
    }
}

pessoa.falar()
````
[Topo](#curso-de-javascript-6)

### **Funções Callback:**
>Primeira explicação.
````javascript
const soma = function (x, y) {
    return x + y
}

const imprimirResultado = function (a, b, operacao = soma) {
    console.log(operacao(a, b))
}

imprimirResultado(3, 4)
imprimirResultado(3, 4, soma)
imprimirResultado(3, 4, function (x, y) {
    return x - y
})
imprimirResultado(3, 4, (x, y) => x * y)

const pessoa = {
    falar: function () {
        console.log('Opa')
    }
}

pessoa.falar()
````
[Topo](#curso-de-javascript-6)

>Segunda explicação.
````javascript
const notas = [7.7, 6.5, 5.2, 8.9, 3.6, 7.1, 9.0]

// Sem callback
const notasBaixas1 = []
for (let i in notas) {
    if (notas[i] < 7) {
        notasBaixas1.push(notas[i])
    }
}

console.log(notasBaixas1)

// Com callback
const notasBaixas2 = notas.filter(function (nota) {
    return nota < 7
})

console.log(notasBaixas2)

const notasMenorQue7 = nota => nota < 7
const notasBaixas3 = notas.filter(notasMenorQue7)
console.log(notasBaixas3)
````
[Topo](#curso-de-javascript-6)

>Terceira explicação.
````javascript
document.getElementsByTagName('body')[0].onclick = function (e) {
    console.log('O evento ocorreu!')
}
````
[Topo](#curso-de-javascript-6)

### **Funções Construtoras:**
>
````javascript
function Carro(velocidadeMaxima = 200, delta = 5) {
    // atributo privado
    let velocidadeAtual = 0

    // metodo publico
    this.acelerar = function () {
        if (velocidadeAtual + delta <= velocidadeMaxima) {
            velocidadeAtual += delta
        } else {
            velocidadeAtual = velocidadeMaxima
        }
    }

    // metodo publico
    this.getVelocidadeAtual = function () {
        return velocidadeAtual
    }
}

const uno = new Carro
uno.acelerar()
console.log(uno.getVelocidadeAtual())

const ferrari = new Carro(350, 20)
ferrari.acelerar()
ferrari.acelerar()
ferrari.acelerar()
console.log(ferrari.getVelocidadeAtual())

console.log(typeof Carro)
console.log(typeof ferrari)
````
[Topo](#curso-de-javascript-6)

### **Tipos de Declaração:**
>
````javascript
console.log(soma(3, 4))

// function declaration
function soma(x, y) {
    return x + y
}

// function expression
const sub = function (x, y) {
    return x - y
}
console.log(sub(3, 4))

// named function expression
const mult = function mult(x, y) {
    return x * y
}
console.log(mult(3, 4))
````
[Topo](#curso-de-javascript-6)

### **Contexto Léxico:**
>Ele vai usar a variavel do escopo em que a função foi criada 
````javascript
const valor = 'Global'

function minhaFuncao() {
    console.log(valor)
}

function exec() {
    const valor = 'Local'
    minhaFuncao()
}

exec()
````
[Topo](#curso-de-javascript-6)

### **Closures:**
>Ele vai usar a variavel do escopo em que a função foi criada 
````javascript
/ Closure é o escopo criado quando uma função é declarada
// Esse escopo permite a função acessar e manipular variáveis externas à função

// Contexto léxico em ação!

const x = 'Global'

function fora() {
    const x = 'Local'
    function dentro() {
        return x
    }
    return dentro
}

const minhaFuncao = fora()
console.log(minhaFuncao())
````
[Topo](#curso-de-javascript-6)

### **Função Factory:**
>Função factory é sempre uma função que cria e retorna um objeto
````javascript
// Factory simples
function criarPessoa() {
    return {
        nome: 'Ana',
        sobrenome: 'Silva'
    }
}

console.log(criarPessoa())
````
[Topo](#curso-de-javascript-6)

>
````javascript
function criarProduto(nome, preco) {
    return {
        nome,                  //A ausencia de nome dos atributos é pq o nome do atributo é o mesmo do parametro
        preco,
        desconto: 0.1
    }
}

console.log(criarProduto('Notebook', 2199.49))
console.log(criarProduto('iPad', 1199.49))
````
[Topo](#curso-de-javascript-6)

### **Class vs Factory:**
>
````javascript
class Pessoa {
    constructor(nome) {
        this.nome = nome
    }

    falar() {
        console.log(`Meu nome é ${this.nome}`)
    }
}

const p1 = new Pessoa('João')
p1.falar()

const criarPessoa = nome => {
    return {
        falar: () => console.log(`Meu nome é ${nome}`)
    }
}

const p2 = criarPessoa('João')
p2.falar()
````
[Topo](#curso-de-javascript-6)

### **IIFE:**
>Função auto envocada para fugir do escopo global
````javascript
// IIFE -> Immediately Invoked Function Expression

(function() {
    console.log('Será executado na hora!')
    console.log('Foge do escopo mais abrangente!')
})()
````
[Topo](#curso-de-javascript-6)

### **Call e Apply:**
>Defininindo contexto e passando parametros
````javascript
function getPreco(imposto = 0, moeda = 'R$') {
    return `${moeda} ${this.preco * (1 - this.desc) * (1 + imposto)}`
}

const produto = {
    nome: 'Notebook',
    preco: 4589,
    desc: 0.15,
    getPreco
}

global.preco = 20
global.desc = 0.1
console.log(getPreco())
console.log(produto.getPreco())

const carro = { preco: 49990, desc: 0.20 }

console.log(getPreco.call(carro))
console.log(getPreco.apply(carro))

console.log(getPreco.call(carro, 0.17, '$'))
console.log(getPreco.apply(global, [0.17, '$']))
````
[Topo](#curso-de-javascript-6)


## 4. **Objeto**

### **Criar objetos:**

>Formas e estratégias de criação de objetos
````javascript
// usando a notação literal
const obj1 = {}
console.log(obj1)

// Object em JS
console.log(typeof Object, typeof new Object)
const obj2 = new Object
console.log(obj2)

// Funções construtoras
function Produto(nome, preco, desc) {
    this.nome = nome
    this.getPrecoComDesconto = () => {
        return preco * (1 - desc)
    }
}

const p1 = new Produto('Caneta', 7.99, 0.15)
const p2 = new Produto('Notebook', 2998.99, 0.25)
console.log(p1.getPrecoComDesconto(), p2.getPrecoComDesconto())

// Função Factory
function criarFuncionario(nome, salarioBase, faltas) { // É uma função que fabrica uma objeto
    return {
        nome,
        salarioBase,
        faltas,
        getSalario() {
            return (salarioBase / 30) * (30 - faltas)
        }
    }
}

const f1 = criarFuncionario('João', 7980, 4)
const f2 = criarFuncionario('Maria', 11400, 1)
console.log(f1.getSalario(), f2.getSalario())

// Object.create
const filha = Object.create(null)
filha.nome = 'Ana'
console.log(filha)

// Um função famosa que retorna Objeto...
const fromJSON = JSON.parse('{"info": "Sou um JSON"}')
console.log(fromJSON.info)

````
[Topo](#curso-de-javascript-6)

### **Objetos Constantes:**

>Congelar o objeto para que não possa ser alterados seus valores de atributo
```javascript
// pessoa -> 123 -> {...}
const pessoa = { nome: 'Joao' }
pessoa.nome = 'Pedro'
console.log(pessoa)

// pessoa -> 456 -> {...}
// pessoa = { nome: 'Ana' }

Object.freeze(pessoa) //Os atributos do objeto não podrão ser alterados apartir desse momento

pessoa.nome = 'Maria'
pessoa.end = 'Rua ABC'
delete pessoa.nome

console.log(pessoa.nome)
console.log(pessoa)

const pessoaConstante = Object.freeze({ nome: 'Joao' }) //Cria o objeto para nunca ser alterado
pessoaConstante.nome = 'Maria'
console.log(pessoaConstante)

```
[Topo](#curso-de-javascript-6)

### **Notação Literal (criando atributos no objeto):**

>Formas de criar atributos e funções nos objetos
```javascript

const a = 1
const b = 2
const c = 3

const obj1 = { a: a, b: b, c: c }
const obj2 = { a, b, c }
console.log(obj1, obj2)

const nomeAttr = 'nota'
const valorAttr = 7.87

const obj3 = {}
obj3[nomeAttr] = valorAttr
console.log(obj3)

const obj4 = {[nomeAttr]: valorAttr}
console.log(obj4)

const obj5 = {
    funcao1: function() {
        // ...
    },
    funcao2() {
        // ...
    }
}
console.log(obj5)

```
[Topo](#curso-de-javascript-6)

### **Getters e Setters**
>Encapsulamento

```javascript
const sequencia = {
    _valor: 1, // convenção
    get valor() { return this._valor++ },
    set valor(valor) { 
        if(valor > this._valor) {
            this._valor = valor
        }
    }
}

console.log(sequencia.valor, sequencia.valor)//O javascript entende que vc está tentando ler entao chama a função get valor()
sequencia.valor = 1000 //O javascript entende que vc está tentando gravar entao chama a função set valor()
console.log(sequencia.valor, sequencia.valor)
sequencia.valor = 900
console.log(sequencia.valor, sequencia.valor)
```
[Topo](#curso-de-javascript-6)

### **Funções Importantes de Objeto**
>Funções para listar, encapsular e atribuir

````javascript

const pessoa = {
    nome: 'Rebeca',
    idade: 2,
    peso: 13
}

console.log(Object.keys(pessoa))//Retorna todas as chaves do objeto
console.log(Object.values(pessoa))//Retorna todos os valores 
console.log(Object.entries(pessoa))//Retorna um array com todas as chaves valor do objeto

Object.entries(pessoa).forEach(([chave, valor]) => {
    console.log(`${chave}: ${valor}`)
})

Object.defineProperty(pessoa, 'dataNascimento', {
    enumerable: true, //Permite listar a propriedade
    writable: false, //Não permite alteração do valor da propriedade, não permite modificação
    value: '01/01/2019' //O valor da propriedade
})// Cria uma propriedade dentro de um objeto com caracteristar definidas

pessoa.dataNascimento = '01/01/2017'
console.log(pessoa.dataNascimento)
console.log(Object.keys(pessoa))

// Object.assign (ECMAScript 2015)
const dest = { a: 1 }
const o1 = { b: 2 }
const o2 = { c: 3, a: 4 }
const obj = Object.assign(dest, o1, o2)//Vai atibuir os atributos de outro objeto para o objeto destino

Object.freeze(obj)
obj.c = 1234
console.log(obj)

````
[Topo](#curso-de-javascript-6)

### **Herança**
>Primeira explicação

````javascript
const ferrari = {
    modelo: 'F40',
    velMax: 324
}

const volvo = {
    modelo: 'V40',
    velMax: 200
}

console.log(ferrari.prototype)
console.log(ferrari.__proto__)
console.log(ferrari.__proto__ === Object.prototype)
console.log(volvo.__proto__ === Object.prototype)
console.log(Object.prototype.__proto__ === null)

function MeuObjeto() {}
console.log(typeof Object, typeof MeuObjeto)
console.log(Object.prototype, MeuObjeto.prototype)

````
[Topo](#curso-de-javascript-6)

>Segunda explicação, criando herança de fato
````javascript
// Cadeia de protótipos (prototype chain)
Object.prototype.attr0 = '0' // não faça isso em casa!

const avo = { attr1: 'A' }
const pai = { __proto__: avo, attr2: 'B', attr3: '3' }// O atributo __proto__ recebe o nome do obejto que irá herdar
const filho = { __proto__: pai, attr3: 'C' }
console.log(filho.attr0, filho.attr1, filho.attr2, filho.attr3)

const carro = {
    velAtual: 0,
    velMax: 200,
    acelerarMais(delta) {
        if (this.velAtual + delta <= this.velMax) {
            this.velAtual += delta
        } else {
            this.velAtual = this.velMax
        }
    },
    status() {
        return `${this.velAtual}Km/h de ${this.velMax}Km/h`
    }
}

const ferrari = {
    modelo: 'F40',
    velMax: 324 // shadowing
}

const volvo = {
    modelo: 'V40',
    status() {
        return `${this.modelo}: ${super.status()}` // Usa-se o super para chmar um metodo ou atributo do elemento pai
    }
}

Object.setPrototypeOf(ferrari, carro)// Outra forna de criar herança. ferrari herda carro.
Object.setPrototypeOf(volvo, carro)

console.log(ferrari)
console.log(volvo)

volvo.acelerarMais(100)
console.log(volvo.status())

ferrari.acelerarMais(300)
console.log(ferrari.status())
````
[Topo](#curso-de-javascript-6)

>Terceira explicação, usando o Object.create()
````javascript
const pai = { nome: 'Pedro', corCabelo: 'preto' }

const filha1 = Object.create(pai) //Cria um objeto novo tendo o objeto pai como prototype(herança)
filha1.nome = 'Ana'
console.log(filha1.corCabelo)

const filha2 = Object.create(pai, {
    nome: { value: 'Bia', writable: false, enumerable: true }
})

console.log(filha2.nome)
filha2.nome = 'Carla'
console.log(`${filha2.nome} tem cabelo ${filha2.corCabelo}`)

console.log(Object.keys(filha1))
console.log(Object.keys(filha2))

for(let key in filha2) {
    filha2.hasOwnProperty(key) ? // Para saber se a propriedade pertence ao proprio objeto ou veio por herança
        console.log(key) : console.log(`Por herança: ${key}`)
}
````
[Topo](#curso-de-javascript-6)

>Quarta explicação, usando o Object.prototype
````javascript
function MeuObjeto() {}
console.log(MeuObjeto.prototype)

const obj1 = new MeuObjeto
const obj2 = new MeuObjeto
console.log(obj1.__proto__ === obj2.__proto__)
console.log(MeuObjeto.prototype === obj1.__proto__)

MeuObjeto.prototype.nome = 'Anônimo'
MeuObjeto.prototype.falar = function() {
    console.log(`Bom dia! Meu nome é ${this.nome}!`)
}

obj1.falar()

obj2.nome = 'Rafael'
obj2.falar()

const obj3 = {}
obj3.__proto__ = MeuObjeto.prototype
obj3.nome = 'Obj3'
obj3.falar()

// Resumindo a loucura...
console.log((new MeuObjeto).__proto__ === MeuObjeto.prototype)
console.log(MeuObjeto.__proto__ === Function.prototype)
console.log(Function.prototype.__proto__ === Object.prototype)
console.log(Object.prototype.__proto__ === null)
````
[Topo](#curso-de-javascript-6)

>Quinta explicação, alterando o prototype padraão
````javascript
console.log(typeof String)
console.log(typeof Array)
console.log(typeof Object)

String.prototype.reverse = function () {
    return this.split('').reverse().join('')
}

console.log('Escola Cod3r'.reverse())

Array.prototype.first = function() {
    return this[0]
}

console.log([1, 2, 3, 4, 5].first())
console.log(['a', 'b', 'c'].first())

String.prototype.toString = function () {
    return 'Lascou tudo'
}

console.log('Escola Cod3r'.reverse())
````
[Topo](#curso-de-javascript-6)

>Sexta explicação, criando o operador new
````javascript
function Aula(nome, videoID) {
    this.nome = nome
    this.videoID = videoID
}

const aula1 = new Aula('Bem Vindo', 123)
const aula2 = new Aula('Até Breve', 456)
console.log(aula1, aula2)

// simulando o new
function novo(f, ...params) {
    const obj = {}
    obj.__proto__ = f.prototype
    f.apply(obj, params)
    return obj
}

const aula3 = novo(Aula, 'Bem Vindo', 123)
const aula4 = novo(Aula, 'Até Breve', 456)
console.log(aula3, aula4)
````
[Topo](#curso-de-javascript-6)

### **Evitando Modificações**
>Evitando que adicionem novos atributos ao seu objeto
````javascript
// Object.preventExtensions Não consegue adicionar, mas consegue excluir
const produto = Object.preventExtensions({
    nome: 'Qualquer', preco: 1.99, tag: 'promoção'
})
console.log('Extensível:', Object.isExtensible(produto))

produto.nome = 'Borracha'
produto.descricao = 'Borracha escolar branca'
delete produto.tag
console.log(produto)

// Object.seal Não consegue adicionar nem excluir
const pessoa = { nome: 'Juliana', idade: 35 }
Object.seal(pessoa)
console.log('Selado:', Object.isSealed(pessoa))

pessoa.sobrenome = 'Silva'
delete pessoa.nome
pessoa.idade = 29
console.log(pessoa)

// Object.freeze = selado + valores constantes
````
[Topo](#curso-de-javascript-6)

### **JSON vs Objeto**
>JSON é apenas texto, carrega apenas dados e não funcionalidades
````javascript
const obj = { a: 1, b: 2, c: 3, soma() { return a + b + c } }
console.log(JSON.stringify(obj))//Converte objeto javascript para JSON

// console.log(JSON.parse("{ a: 1, b: 2, c: 3 }"))
// console.log(JSON.parse("{ 'a': 1, 'b': 2, 'c': 3 }"))
console.log(JSON.parse('{ "a": 1, "b": 2, "c": 3 }'))
console.log(JSON.parse('{ "a": 1.7, "b": "string", "c": true, "d": {}, "e": [] }'))
````
[Topo](#curso-de-javascript-6)

### **Classe**
>As classes criadas em javascript será transformada em função
````javascript
class Lancamento {
    constructor(nome = 'Genérico', valor = 0) {
        this.nome = nome
        this.valor = valor
    }
}

class CicloFinanceiro {
    constructor(mes, ano) {
        this.mes = mes
        this.ano = ano
        this.lancamentos = []
    }

    addLancamentos(...lancamentos) {
        lancamentos.forEach(l => this.lancamentos.push(l))
    }

    sumario() {
        let valorConsolidado = 0
        this.lancamentos.forEach(l => {
            valorConsolidado += l.valor
        })
        return valorConsolidado
    }
}

const salario = new Lancamento('Salario', 45000)
const contaDeLuz = new Lancamento('Luz', -220)

const contas = new CicloFinanceiro(6, 2018)
contas.addLancamentos(salario, contaDeLuz)
console.log(contas.sumario())
````
[Topo](#curso-de-javascript-6)

>Herança em classes
````javascript
class Avo {
    constructor(sobrenome) {
        this.sobrenome = sobrenome
    }
}

class Pai extends Avo {
    constructor(sobrenome, profissao = 'Professor') {
        super(sobrenome)
        this.profissao = profissao
    }
}

class Filho extends Pai {
    constructor() {
        super('Silva')
    }
}

const filho = new Filho
console.log(filho)
````
[Topo](#curso-de-javascript-6)

## 5. **Array**

### **Visão Geral**
>O array em javascript é um objeto. Não existe um tipo nativo do tipo array.

````javascript
console.log(typeof Array, typeof new Array, typeof [])

let aprovados = new Array('Bia', 'Carlos', 'Ana')
console.log(aprovados)

aprovados = ['Bia', 'Carlos', 'Ana']
console.log(aprovados[0])
console.log(aprovados[1])
console.log(aprovados[2])
console.log(aprovados[3])

aprovados[3] = 'Paulo'
aprovados.push('Abia')
console.log(aprovados.length)

aprovados[9] = 'Rafael'
console.log(aprovados.length)
console.log(aprovados[8] === undefined)

console.log(aprovados)
aprovados.sort()
console.log(aprovados)

delete aprovados[1]
console.log(aprovados[1])
console.log(aprovados[2])

aprovados = ['Bia', 'Carlos', 'Ana']
aprovados.splice(1, 1)
console.log(aprovados)
````
[Topo](#curso-de-javascript-6)

### **Métodos Importantes**
>

````javascript
const pilotos = ['Vettel', 'Alonso', 'Raikkonen', 'Massa']
pilotos.pop() // massa quebrou o carro!
console.log(pilotos)

pilotos.push('Verstappen')
console.log(pilotos)

pilotos.shift() // remove o primeiro!
console.log(pilotos)

pilotos.unshift('Hamilton')
console.log(pilotos)

// splice pode adicionar e remover elementos

// adicionar
pilotos.splice(2, 0, 'Bottas', 'Massa')
console.log(pilotos)

// remover
pilotos.splice(3, 1) // massa quebrou :(
console.log(pilotos)

const algunsPilotos1 = pilotos.slice(2) // Retorna um novo array apartir do indice passado por parametro
console.log(algunsPilotos1)

const algunsPilotos2 = pilotos.slice(1, 4)
console.log(algunsPilotos2)
````
[Topo](#curso-de-javascript-6)

### **Simulando Array com Objeto**
>

````javascript
const quaseArray = { 0: 'Rafael', 1: 'Ana', 2: 'Bia' }
console.log(quaseArray)
Object.defineProperty(quaseArray, 'toString', {
    value: function() { return Object.values(this) },
    enumerable: false
})

console.log(quaseArray[0])

const meuArray = ['Rafael', 'Ana', 'Bia']
console.log(quaseArray.toString(), meuArray)
````
[Topo](#curso-de-javascript-6)

### **Foreach**
>Percorrer um Array

````javascript
const aprovados = ['Agatha', 'Aldo', 'Daniel', 'Raquel']

aprovados.forEach(function(nome, indice) {
    console.log(`${indice + 1}) ${nome}`)
})

aprovados.forEach(nome => console.log(nome))

const exibirAprovados = aprovado => console.log(aprovado)
aprovados.forEach(exibirAprovados)
````
[Topo](#curso-de-javascript-6)

>Emplementando um forEach

````javascript
Array.prototype.forEach2 = function(callback) {
    for (let i = 0; i < this.length; i++) {
        callback(this[i], i, this)
    }
}

const aprovados = ['Agatha', 'Aldo', 'Daniel', 'Raquel']

aprovados.forEach2(function(nome, indice) {
    console.log(`${indice + 1}) ${nome}`)
})
````
[Topo](#curso-de-javascript-6)

### **Map**
>Primeira explicação. O map retorna um outro Array com os dados transformados basedo no array original.

````javascript
const nums = [1, 2, 3, 4, 5]

// For com propósito
let resultado = nums.map(function(e) { //A função callBack pode receber tres parametros: o valor do elemento, indice e o Array completo
    return e * 2                       //Lembrando que a função callBack deve ter um retorno
})

console.log(resultado)

const soma10 = e => e + 10
const triplo = e => e * 3
const paraDinheiro = e => `R$ ${parseFloat(e).toFixed(2).replace('.', ',')}`

resultado = nums.map(soma10).map(triplo).map(paraDinheiro)
console.log(resultado)
````
[Topo](#curso-de-javascript-6)

>Segunda explicação.
````javascript
const carrinho = [
    '{ "nome": "Borracha", "preco": 3.45 }',
    '{ "nome": "Caderno", "preco": 13.90 }',
    '{ "nome": "Kit de Lapis", "preco": 41.22 }',
    '{ "nome": "Caneta", "preco": 7.50 }'
]

// Retornar um array apenas com os preços

const paraObjeto = json => JSON.parse(json)
const apenasPreco = produto => produto.preco

const resultado = carrinho.map(paraObjeto).map(apenasPreco)
console.log(resultado)
````
[Topo](#curso-de-javascript-6)

>Terceira explicação. Implementando um map
````javascript
Array.prototype.map2 = function(callback) {
    const newArray = []
    for (let i = 0; i < this.length; i++) {
        newArray.push(callback(this[i], i, this))
    }
    return newArray
}

const carrinho = [
    '{ "nome": "Borracha", "preco": 3.45 }',
    '{ "nome": "Caderno", "preco": 13.90 }',
    '{ "nome": "Kit de Lapis", "preco": 41.22 }',
    '{ "nome": "Caneta", "preco": 7.50 }'
]

// Retornar um array apenas com os preços

const paraObjeto = json => JSON.parse(json)
const apenasPreco = produto => produto.preco

const resultado = carrinho.map2(paraObjeto).map2(apenasPreco)
console.log(resultado)
````
[Topo](#curso-de-javascript-6)

### **Filter**
>Primeira explicação. Retorna uma Array somente com os elementos que foram validados. Os que retornam TRUE permanecem e os que retornam FALSE são eliminados.
````javascript
const produtos = [
    { nome: 'Notebook', preco: 2499, fragil: true },
    { nome: 'iPad Pro', preco: 4199, fragil: true },
    { nome: 'Copo de Vidro', preco: 12.49, fragil: true },
    { nome: 'Copo de Plástico', preco: 18.99, fragil: false }
]

console.log(produtos.filter(function(p) {
    return false
}))

const caro = produto => produto.preco >= 500
const fragil = produto => produto.fragil

console.log(produtos.filter(caro).filter(fragil))
````
[Topo](#curso-de-javascript-6)

>Segunda explicação. Implementando Filter
````javascript
Array.prototype.filter2 = function(callback) {
    const newArray = []
    for (let i = 0; i < this.length; i++) {
        if(callback(this[i], i, this)) {
            newArray.push(this[i])
        }
    }
    return newArray
}

const produtos = [
    { nome: 'Notebook', preco: 2499, fragil: true },
    { nome: 'iPad Pro', preco: 4199, fragil: true },
    { nome: 'Copo de Vidro', preco: 12.49, fragil: true },
    { nome: 'Copo de Plástico', preco: 18.99, fragil: false }
]

const caro = produto => produto.preco >= 500
const fragil = produto => produto.fragil

console.log(produtos.filter2(caro).filter2(fragil))
````
[Topo](#curso-de-javascript-6)

### **Reduce**
>Primeira explicação.Ele percorre um arrei acumulando valores e retorna o resultado dos valores acumulados. Agrega valores
````javascript
const alunos = [
    { nome: 'João', nota: 7.3, bolsista: false },
    { nome: 'Maria', nota: 9.2, bolsista: true },
    { nome: 'Pedro', nota: 9.8, bolsista: false },
    { nome: 'Ana', nota: 8.7, bolsista: true }
]

console.log(alunos.map(a => a.nota))
const resultado = alunos.map(a => a.nota).reduce(function(acumulador, atual) {
    console.log(acumulador, atual)
    return acumulador + atual
}, 0)// Se não quiser que o aculador nao inicie com nenhum valor, deixe o segundo parametro com o valor 0.

console.log(resultado)
````
[Topo](#curso-de-javascript-6)

>Segunda explicação.
````javascript
const alunos = [
    { nome: 'João', nota: 7.3, bolsista: false },
    { nome: 'Maria', nota: 9.2, bolsista: true },
    { nome: 'Pedro', nota: 9.8, bolsista: false },
    { nome: 'Ana', nota: 8.7, bolsista: true }
]

// Desafio 1: Todos os alunos são bolsista?
const todosBolsistas = (resultado, bolsista) => resultado && bolsista
console.log(alunos.map(a => a.bolsista).reduce(todosBolsistas))

// Desafio 2: Algum aluno é bolsista?
const algumBolsista = (resultado, bolsista) => resultado || bolsista
console.log(alunos.map(a => a.bolsista).reduce(algumBolsista))

````
[Topo](#curso-de-javascript-6)

>Terceira explicação. Implementando Reduce
````javascript
Array.prototype.reduce2 = function(callback, valorInicial) {
    const indiceInicial = valorInicial ? 0 : 1
    let acumulador = valorInicial || this[0]
    for (let i = indiceInicial; i < this.length; i++) {
        acumulador = callback(acumulador, this[i], i, this)
    }
    return acumulador
}

const soma = (total, valor) => total + valor
const nums = [1, 2, 3, 4, 5, 6]
console.log(nums.reduce2(soma, 21))
````
[Topo](#curso-de-javascript-6)

### **Concat**
>Concatenar um array em um unico array.

````javascript
const filhas = ['Ualeskah', 'Cibalena']
const filhos = ['Uoxiton', 'Uesclei']
const todos = filhas.concat(filhos)
console.log(todos, filhas, filhos)

console.log([].concat([1, 2], [3, 4], 5, [[6, 7]]))
````
[Topo](#curso-de-javascript-6)

### **FlatMap**
>O flatMap não é uma API nativa do javascript

````javascript
const escola = [{
    nome: 'Turma M1',
    alunos: [{
        nome: 'Gustavo',
        nota: 8.1
    }, {
        nome: 'Ana',
        nota: 9.3
    }]
}, {
    nome: 'Turma M2',
    alunos: [{
        nome: 'Rebeca',
        nota: 8.9
    }, {
        nome: 'Roberto',
        nota: 7.3
    }]
}]

const getNotaDoAluno = aluno => aluno.nota
const getNotasDaTurma = turma => turma.alunos.map(getNotaDoAluno)

const notas1 = escola.map(getNotasDaTurma)
console.log(notas1)

console.log([].concat([ 8.1, 9.3 ], [ 8.9, 7.3 ]))

Array.prototype.flatMap = function(callback) {
    return Array.prototype.concat.apply([], this.map(callback))
}

const notas2 = escola.flatMap(getNotasDaTurma)
console.log(notas2)
````
[Topo](#curso-de-javascript-6)
