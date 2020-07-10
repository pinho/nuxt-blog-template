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
  font-family:  Arial, sans-serif;
  font-size: 11pt;
}
.markdown-body > h1 {
  text-align: center;
  font-size: 40px;
  font-weight: 600;
  padding-block: 2rem;
}
.markdown-body > h2 {
  margin-block: 36px 10px;
}
.markdown-body > h2::before {
  content: '## ';
  color: #00C58E;
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
  color: #108775;
}
.markdown-body blockquote {
  background-color: #fff;
  font-family: 'Times New Roman', serif;
  font-style: italic;
  font-size: 13pt;
  padding: 26px 48px;
  border-left: 6px solid #2F495E;
  color: #2F495E;
  box-sizing: content-box;
}
.markdown-body code {
  box-sizing: border-box;
  font-family: monospace;
  font-size: .9em;
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