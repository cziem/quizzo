<template>
  <div class="app">
    <app-header></app-header>
    <app-quiz></app-quiz>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Quiz from "./components/Quiz.vue";

export default {
  components: {
    "app-header": Header,
    "app-quiz": Quiz
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
