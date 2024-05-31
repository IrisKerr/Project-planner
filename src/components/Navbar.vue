<template>
  <nav class="main-nav">
    <router-link :to="{ name: 'Home' }">Projects</router-link>
    <router-link :to="{ name: 'AddProject' }">Add a new Project</router-link>
  </nav>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Navbar",
};
</script>

<style>
.main-nav {
  text-align: center;
  margin: 40px auto;
}

.main-nav a {
  display: inline-block;
  text-decoration: none;
  margin: 0 10px;
  color: #999;
  font-size: 20px;
}

a.router-link-active {
  border-bottom: 2px solid #00ce89af;
  padding-bottom: 4px;
}
</style>
