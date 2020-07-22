<template>
  <div class="container">
    <navbar />
    <div class="internal-container">
      <h1 class="title default-font">My posts</h1>
      <ul class="list-of-posts">
        <li v-for="post in posts" :key="post.attributes.title" class="l-item">
          <nuxt-link :to="getPermalink(post)">
            <logo/>
            <div class="text-container">
              <h1 class="post-title default-font">
                {{ post.attributes.title }}
              </h1>
              <p v-if="post.attributes.author" class="author-name default-font">
                Written by {{ post.attributes.author }}
              </p>
              <p v-if="post.attributes.brief" class="brief default-font">
                {{ post.attributes.brief }}
              </p>
            </div>
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Navbar from '~/components/Navbar.vue'

export default {
  async asyncData() {
    const resolve = require.context("~/articles/", true, /\.md$/);
    const imports = resolve.keys().map(key => {
      const [, name] = key.match(/\/(.+)\.md$/);
      return resolve(key);
    });
    return {
      posts: imports
    };
  },
  data() {
    return {
      prefix: 'blog'
    }
  },
  methods: {
    getPermalink(post) {
        return `/blog/${post.attributes.slug}`;
    }
  },
  components: {
    Logo,
    Navbar
  }
};
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

.internal-container {
  width: 60%;
}

.title {
  display: block;
  font-weight: 300;
  font-size: 30px;
  color: #35495e;
  letter-spacing: 1px;
  padding: .5em 0;
}

.list-of-posts {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  padding: 0;
  width: 100%;
  min-width: 50%;
}

.l-item {
  list-style: none;
  padding: 12px 8px;
  margin: 4px auto;
  border: 1px solid white;
  width: 80%;
  border-radius: 8px;
  transition: all .25s;
}
.l-item:hover {
  border: 1px solid #108775;
}

.l-item > * {
  display: flex;
}

.text-container {
  padding: .8em 24px;
  width: 70%;
}

.default-font {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-weight: 400;
}

.post-title {
  font-size: 18pt;
  color: #35495e;
  text-align: left;
  line-height: 1.1em;
}

.author-name {
  color: #35495eaa;
  font-weight: 400;
  font-size: 11pt;
  text-align: left;
  line-height: 2.2em;
}

.brief {
  font-size: 12pt;
  font-weight: 400;
  color: #35495e;
  text-align: left;
  overflow-y: hidden;
  overflow-x: hidden;
  max-height: 50%;
}
</style>