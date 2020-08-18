<template>
  <div class="user">
    <h1>{{ this.$route.params.id }}</h1>
    <router-link :to="{name: 'first'}">first</router-link> |
    <router-link :to="{name: 'second'}">second</router-link>
    <router-view/>
  </div>
</template>

<style scoped>
  .router-link-exact-active {
    font-size: 25px;
    color: red;
  }
</style>
