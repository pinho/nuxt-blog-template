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
  width: 75%;
  max-width: 920px;
  min-width: 720px;
  margin: 0 auto;
  padding: 48px 5rem;
}

.markdown-body {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 12pt;
  font-weight: 400;
  color: #35495e;
}

.markdown-body > h1 {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  text-align: center;
  font-size: 50px;
  font-weight: 400;
  padding-block: 1.5em;
}

.markdown-body > h2 {
  font-weight: 400;
  margin-block: 36px 10px;
}
.markdown-body > h2::before {
  content: '## ';
  color: #00C58E;
}

.markdown-body > h3 {
  font-weight: 400;
  font-size: 15pt;
}

.markdown-body > p {
  text-align: justify;
  font-size: 12pt;
  margin-block: 1.2rem;
  line-height: 1.3em;
  color: #121;
}

.markdown-body a {
  color: grey;
}
.markdown-body a:hover {
  color: #108775;
}

.markdown-body blockquote {
  background-color: #cccece;
  width: 75%;
  margin: 0 auto;
  border-radius: 4px;
  font-family: 'Times New Roman', serif;
  color: #111;
  font-style: italic;
  font-size: 13pt;
  padding: 20px 48px;
  box-sizing: content-box;
}

.markdown-body code {
  box-sizing: border-box;
  font-family: monospace;
  font-size: .9em;
  color: #35495e;
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
  color: #15293e;
  font-size: 10pt;
}
</style>