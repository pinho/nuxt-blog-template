<template>
  <nav class="navmenu">
    <ul class="menulist">
      <nuxt-link to='/'>
        <li class="menu-item">Home</li>
      </nuxt-link>
      <nuxt-link to='/blog'>
        <li class="menu-item">Blog</li>
      </nuxt-link>
    </ul>
  </nav>
</template>

<script>
export default {

}
</script>

<style>
.navmenu {
  width: 100%;
  padding: 32px 8px;
  width: 100%;
  position: static;
  top: 0;
}

.menulist {
  display: flex;
  justify-content: space-around;
  width: 60%;
  padding: 0;
  margin: 0 auto;
}

.menu-item {
  color: #35465a;
  padding: .4em 1em;
  list-style: none;
  text-decoration: none;
  font-weight: 600;
  font-size: 14pt;
  transition: all 0.2s;
}
.menu-item:hover {
  color: white;
  background-color: #108775;
}

a {
  text-decoration: none;
}
</style>