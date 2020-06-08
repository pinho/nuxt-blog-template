<template>
  <div>
    <h1>My blog posts</h1>
    <ul>
      <li v-for="post in posts" :key="post.attributes.title">
        <nuxt-link v-bind:to="getPermalink(post)">
          {{ post.attributes.slug }}
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
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
  }
};
</script>