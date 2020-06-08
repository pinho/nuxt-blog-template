# nuxt-blog-template

> A template for blog project in Nuxt.js and Markdown

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

## Usage

This project aims to manage blog posts in markdown. All post should be placed in
`articles` directory and have a slug because it defines the "id" which is used
to access the post via link. For example:

```
---
slug: my-post
---

# An awesome post

...
```

This post is accessed using: `http://yoursite.example/blog/my-post`

## Links

For detailed explanation on how things work, check out
[Nuxt.js docs](https://nuxtjs.org).
