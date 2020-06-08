---
slug: steps
title: Creating this repo template
author: Ronaldd Pinho
---

# Creating this repo template

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
adicionada ao `nuxt.config.js`, esse diretório será usado para armazenar os 
arquivos markdown referentes às postagens. Crie um arquivo markdown para teste
dentro desse diretório.

```zsh
% mkdir articles
% echo "Hello, World" > articles/hello.md
```

No diretório `pages` crie um subdiretório com o nome que deseja para a rota dos
posts, nesse caso, criei diretório chamado `./pages/blog` dessa forma o link
para as postagens fica `http://yoursite/blog/post-name`.

```zsh
% mkdir pages/blog
```

Nesse diretório é criado um arquivo `index.vue` que define a página inicial do
blog que lista todos os posts, e um arquivo `_slug.vue` que define uma página
que será usada como template para todos os posts em `./articles`.

```zsh
% touch pages/blog/{index,_slug}.vue
```

Criar o layout de um artigo em `./layouts/`, esse arquivo definirá o modelo (
elementos e estilo) das páginas de posts.
```zsh
% touch layouts/article.vue
```

O código adicionado aqui é simples:
```html
<template>
  <div id="articleContainer">
    <nuxt/>
  </div>
</template>

<script>
export default {
  layout: 'article'
}
</script>

<style>
/* Use a linguagem da sua preferência para estilos do template */
</style>
```

Adicionar o código dos arquivos vue no diretório `pages/blog`.

## Links

Siga-me nas mídias sociais:

* @ronalddpinho on [Twitter](https://twitter.com/ronalddpinho)
* @pinho on [Github](https://github.com/pinho)
