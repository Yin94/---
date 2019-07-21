<template>
  <div id="app">
    <NavBar v-on:searched="searchedHandler"></NavBar>
    <router-view />
  </div>
</template>
<script>
import NavBar from "./components/NavBar.vue";
export default {
  components: {
    NavBar
  },
  methods: {
    searchedHandler(input) {
      this.$router.push(`/items?focus=${input}`);
    }
  }
};
</script>

<style>
@import "~bootstrap/dist/css/bootstrap.css";
</style>
