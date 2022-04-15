## Babel

> Babel : Serve para converter o nosso código para uma  maneira que todos os browsers e todo ambiente de nossa aplicação consiga entender todos os códigos e qual o motivo disso. <br> O Javascript é uma linguagem que se atualiza muito e tem várias  funcionalidades como o React por exemplo a escrita do HTML dentro do própio código javascript que os navegadores ainda não entendem, então o babel faz o papel de converter o nosso código para uma maneira que os navegadores mais modernos possam entender esse código.

> Plataforma do Babel
- https://babeljs.io/

> Passo 1 : Adicionando o Babel a uma projeto como dependência de desenvolvimento.

```bash
yarn add @babel/core @babel/cli @babel/preset-env -D
```

> Passo 2 : Após instalar essas bibliotecas deve criar na raiz do projeto um arquivo chamado babel.config.js e adicionar as configurações abaixo.

- @babel/core : A biblioteca principal do babel, 90% das funcionalidades do babel está nela.

- @babel/cli : É uma biblioteca para conseguir executar o babel através da linha de comando.

- @babel/preset-env : É uma biblioteca que identifica em qual ambiente a aplicação está sendo executada para converter a aplicação da melhor maneira possível.

```js

// babel.config.js

module.exports = {
    presets: [
        '@babel/preset-env'
    ]
}
```

> Testando o babel

- Crie um arquivo javascript e adicione algum trecho de código após isso execute a linha de comando abaixo.

```js

// src/index.js

const user = {
    name: 'Anderson'
}

console.log(user.address.street);
```

```bash
yarn babel src/index.js --out-file <nome-arquivo-relativo>
```

> Passo 3 : Adicionando algumas bibliotecas do Babel para uma aplicação React ser compilada pelo babel.

```bash
yarn add @babel/preset-react -D
```

```js

// babel.config.js

module.exports = {
    presets: [
        '@babel/preset-env',
        '@babel/preset-react'
    ]
}
```

- Com isso temos a estrutura do babel configurada para se trabalhar com aplicações javascrip ou react de uma maneira moderna.