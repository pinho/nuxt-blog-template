<template>
  <component :is="singlePostComponent" />
</template>

<script>
export default {
  layout: 'article',
  async asyncData({ params }) {
    try {
      console.info(params.slug);
      let post = await import(`~/articles/${params.slug}.md`);
      return {
        title: post.attributes.title,
        singlePostComponent: post.vue.component
      };
    } catch (err) {
      console.debug(err);
      return false;
    }
  }
};
</script>