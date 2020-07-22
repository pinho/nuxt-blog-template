---
slug: step-by-step
title: Step by step for the creation of this repository template
author: R. Pinho
brief: "
This post explains all the steps to create a blog in Nuxt using a markdown loader
"
---

# Step by step for the creation of this repository template 

> Step-by-step to create of this template repository

## Init the project

The project was created using the following `yarn` command:

```zsh
% yarn create nuxt-app nuxt-blog-template
```

After create the Nuxt project, add the package `frontmatter-markdown-loader` as dependencie
```zsh
% yarn add frontmatter-markdown-loader
```

## Configure markdown loader and directory for the posts

Add the `frontmatter-markdown-loader` on configurations, in `nuxt.config.js`, 
add the following code on `build` field:

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
Don't forget import the needed modules:

```js
import path from 'path';
import FMMode from 'frontmatter-markdown-loader/mode';
```

In case of doubts, see the complete file on repository dir. tree.

### Articles directory

Create the `articles` directory, this name was defines on the "include" field
in rule added to `nuxt.config.js`, this directory will be used to store all
markdown files referent to posts. Create a markdown file to tests into this folder.

```zsh
% mkdir articles
% echo "Hello, World" > articles/hello.md
```

## Pages and Layouts

In the `pages` directory, create a subdirectory with the name desired to the route
to posts, in this case, I created a directory called `pages/blog`, so, the links
to posts are link this: `http://yoursite/blog/post-name`.

```zsh
% mkdir pages/blog
```

In this directory was created a file `index.vue` which defines the main blog
page where the posts all listed and, a file `_slug.vue` which serve as
wrapper to the files of content in `articles` folder.

```zsh
% touch pages/blog/{index,_slug}.vue
```

Create a layout for post pages in `./layouts/` directory, this file defines the
template (html elements and css style) of the post pages.
```zsh
% touch layouts/article.vue
```

The code added here is simple:
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
/* Use your prefered language for styles */
</style>
```

Add the code of Vue files in the directory `pages/blog`.
Add content (posts) using markdown files in the directory `articles`.

## Links

Follow-me on social networks:

* @ronalddpinho on [Twitter](https://twitter.com/ronalddpinho)
* @pinho on [Github](https://github.com/pinho)
