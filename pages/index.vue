<template>
  <div class="container">
    <navbar />
    <div>
      <logo />
      <h1 class="title">
        nuxt-blog-template
      </h1>
      <h2 class="subtitle">
        A template for blog project in Nuxt.js and Markdown
      </h2>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Logo,
    Navbar
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 70px;
  color: #35495e;
  letter-spacing: 1px;
  padding: 0;
  margin-bottom: .3em;
}

.subtitle {
  font-weight: 300;
  font-size: 32px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 25px;
}

.links {
  display: flex;
  padding: 15px;
  width: 100%;
  justify-content: space-between;
}
</style>
