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
}
.markdown-body {
  font-family: 'Quicksand', 'Fira Sans', Arial, sans-serif;
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
  margin-block: 1.2rem;
  line-height: 1.5rem;
}
.markdown-body a {
  color: grey;
}
.markdown-body a:hover {
  color: orangered;
}
.markdown-body blockquote {
  background-color: #ddd;
  font-style: italic;
  padding: 1.1rem 2rem;
  border-left: 20px solid #3b8070;
  box-sizing: content-box;
}
.markdown-body code {
  box-sizing: border-box;
  font-family: 'Fira Code', 'Source Code Pro', monospace, sans-serif;
  font-size: 12pt;
  color: #3b8070;
}
.markdown-body > pre {
  width: 100%;
  background-color: #1b3220;
  color: lightgreen;
  padding: 1rem;
  border-radius: .3rem;
  overflow-x: scroll;
}
.markdown-body > pre > code {
  color: whitesmoke;
}
</style>