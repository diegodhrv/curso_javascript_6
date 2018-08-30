## Curso de Javascrip 6

### 1. **Fundamentos**
### 2. **Estrutura de controle**
### 3. **Função**
### 4. **Objeto**

**Objetos Constates:**

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

**Notação Literal (criando atributos no objeto):**

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



### 5. **Array**
