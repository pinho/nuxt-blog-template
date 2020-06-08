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
#articleContainer {
  width: 70%;
  max-width: 920px;
  min-width: 720px;
  margin: 0 auto;
  padding: 48px 5rem;
  border: 1px solid #aaa;
}
.markdown-body {
  font-family: 'Times New Roman', Times, serif;
}
.markdown-body > h1 {
  text-align: center;
  font-size: 40px;
  font-weight: 600;
  padding-block: 2rem;
}
.markdown-body > h2::before {
  content: '## ';
}
.markdown-body > p {
  text-align: justify;
  font-size: 13pt;
  font-family: 'Fira Sans';
  margin-block: .8rem;
  line-height: 1.5rem;
}
.markdown-body > a {
  color: grey;
}
.markdown-body > a:hover {
  color: orangered;
}
</style>