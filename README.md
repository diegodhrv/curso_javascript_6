# Curso de Javascrip 6

## 1. **Fundamentos**
## 2. **Estrutura de controle**
## 3. **Função**
## 4. **Objeto**

### **Objetos Constates:**

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

### **Herança**
>Primeira explicação

`````javascript
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
>Segunda explicação, criando herança de fato
````javascript
// Cadeia de protótipos (prototype chain)
Object.prototype.attr0 = '0' // não faça isso em casa!

const avo = { attr1: 'A' }
const pai = { __proto__: avo, attr2: 'B', attr3: '3' }
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
        return `${this.modelo}: ${super.status()}`
    }
}

Object.setPrototypeOf(ferrari, carro)
Object.setPrototypeOf(volvo, carro)

console.log(ferrari)
console.log(volvo)

volvo.acelerarMais(100)
console.log(volvo.status())

ferrari.acelerarMais(300)
console.log(ferrari.status())

````
## 5. **Array**
