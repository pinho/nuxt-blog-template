# Steps to create 

> Passo a passo do processo de criação desse template

O diretório foi criado usando o yarn, com o comando:
```zsh
% yarn create nuxt-app nuxt-blog-template
```

Após criar o projeto Nuxt, adicione o pacote `frontmatter-markdown-loader` como
dependência.
```zsh
% yarn add frontmatter-markdown-loader
```

Adicione o frontmatter-markdown-loader nas configurações do Nuxt.
No arquivo `nuxt.config.js`, adicione o seguinte código no campo build:

```js
extend (config, ctx) {
  config.module.rules.push({
    test: /\.md$/,
    loader: 'frontmatter-markdown-loader',
    include: path.resolve(__dirname, "articles"), // defines local of md files
    options: {
      mode: [ FMMode.VUE_COMPONENT, FMMode.META ],
      vue: {
        root: 'markdown-body'
      }
    }
  });
}
```
Não esquecendo de importar os módulos necessários

```js
import path from 'path';
import FMMode from 'frontmatter-markdown-loader/mode';
```

Em caso de dúvidas veja o arquivo completo no diretório do projeto.

Crie o diretório `articles`, nome definido no campo "include" da regra
adicionada ao `nuxt.config.js`
```zsh
% mkdir articles
```


