<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link :to="{ name: 'DivNews' }">DivNews</router-link>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>