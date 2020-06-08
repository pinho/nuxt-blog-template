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

<style lang="scss">
// $background: #222;

#articleContainer {
  width: 70%;
  max-width: 920px;
  min-width: 720px;
  margin: 0 auto;
  padding: 48px 5rem;
  border: 1px solid #aaa;

  .markdown-body {
    font-family: 'Times New Roman', Times, serif;

    h1 {
      text-align: center;
      font-size: 40px;
      font-weight: 600;
      padding-block: 2rem;
    }

    h2::before {
      content: '## ';
    }

    p {
      text-align: justify;
      font-size: 13pt;
      font-family: 'Fira Sans';
      margin-block: .8rem;
      line-height: 1.5rem;
      // border: 1px solid blue;
    }

    a {
      color: grey;
    }
    a:hover {
      color: orangered;
    }
  }
}
</style>