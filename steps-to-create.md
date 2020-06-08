# Steps to create 

> Passo a passo do processo de criação desse template

O diretório foi criado usando o yarn, com o comando:
```
yarn create nuxt-app nuxt-blog-template
```

Após criar o projeto Nuxt, adicione o pacote `frontmatter-markdown-loader` como
dependência.
```
yarn add frontmatter-markdown-loader
```

Adicione o frontmatter-markdown-loader nas configurações do Nuxt.
No arquivo `nuxt.config.js`, adicione:

```js
import path from 'path';
import FMMode from 'frontmatter-markdown-loader/mode';

/** code */

  /*
  ** Build configuration
  */
  build: {
    /*
    ** You can extend webpack config here
    */
    extend (config, ctx) {
      config.module.rules.push({
        test: /\.md$/,
        loader: 'frontmatter-markdown-loader',
        include: path.resolve(__dirname, "articles"),
        options: {
          mode: [ FMMode.VUE_COMPONENT ],
          vue: {
            root: 'markdown-body'
          }
        }
      });
    }
  }
```
