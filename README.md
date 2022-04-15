## Babel

> Babel : Serve para converter o nosso código para uma  maneira que todos os browsers e todo ambiente de nossa aplicação consiga entender todos os códigos e qual o motivo disso. <br> O Javascript é uma linguagem que se atualiza muito e tem várias  funcionalidades como o React por exemplo a escrita do HTML dentro do própio código javascript que os navegadores ainda não entendem, então o babel faz o papel de converter o nosso código para uma maneira que os navegadores mais modernos possam entender esse código.

> Plataforma do Babel
- https://babeljs.io/

> Adicionando o Babel a uma aplicação React como dependência de desenvolvimento.

```bash
yarn add @babel/core @babel/cli @babel/preset-env -D
```

> Após instalar essas bibliotecas deve criar na raiz do projeto um arquivo chamado babel.config.js e adicionar as configurações abaixo.

- @babel/core : A biblioteca principal do babel, 90% das funcionalidades do babel está nela.

- @babel/cli : É uma biblioteca para conseguir executar o babel através da linha de comando.

- @babel/preset-env : É uma biblioteca que identifica em qual ambiente a aplicação está sendo executada para converter a aplicação da melhor maneira possível.

```js
module.exports = {
    presets: [
        '@babel/preset-env'
    ]
}
```

