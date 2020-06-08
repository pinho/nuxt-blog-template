<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        nuxt-blog-template
      </h1>
      <h2 class="subtitle">
        A template for blog project in Nuxt.js and Markdown
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >
          Nuxt Documentation
        </a>
        <a
          href="https://github.com/pinho/nuxt-blog-template"
          target="_blank"
          class="button--grey"
        >
          GitHub of Template
        </a>
      </div>
      <div class="links">
        <a
          href="https://twitter.com/ronalddpinho"
          target="_blank"
          class="button--blue"
        >
          Follow author on Twitter
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
