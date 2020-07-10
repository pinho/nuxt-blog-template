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
  font-size: 11pt;
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
  background-color: #efefef;
  font-family: 'Times New Roman', serif;
  font-style: italic;
  font-size: 13pt;
  padding: 30px 48px;
  border-left: 10px solid #108775;
  box-sizing: content-box;
}
.markdown-body code {
  box-sizing: border-box;
  font-family: 'Fira Code', 'Source Code Pro', monospace, sans-serif;
  color: #3b8070;
}
.markdown-body > pre {
  width: 100%;
  background-color: #eeefef;
  color: lightgreen;
  padding: 1rem;
  border-radius: 4px;
  /* overflow-x: scroll; */
}
.markdown-body > pre > code {
  color: darkslategray;
  font-size: 10pt;
}
</style>