<template>
  <div class="app">
    <app-header></app-header>
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  components: {
    "app-header": Header
  },

  data: function() {
    return {};
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.app {
  background: #57b883;
  height: 100vh;
}
</style>
