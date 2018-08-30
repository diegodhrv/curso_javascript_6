## Curso de Javascrip 6

### 1. **Fundamentos**
### 2. **Estrutura de controle**
### 3. **Função**
### 4. **Objeto**

**Objetos Constates:**

Congelar o objeto:
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



5. **Array**
