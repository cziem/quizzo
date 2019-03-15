<template>
  <div class="quiz-body clearfix">
    <div class="quiz-list">
      <quiz-list v-show="isPlaying"></quiz-list>
    </div>
    <div class="btn-group controls">
      <button v-on:click="isPlaying = !isPlaying" v-show="!isPlaying">Start</button>
      <button v-on:click="isPlaying = !isPlaying" v-show="isPlaying">Stop Quiz</button>
    </div>
  </div>
</template>

<script>
import QuizList from "./QuizList.vue";
export default {
  components: {
    "quiz-list": QuizList
  },

  name: "Quiz",
  data() {
    return {
      isPlaying: false
    };
  }
};
</script>

<style scoped>
.clearfix {
  margin: 1rem auto;
}

.quiz-body {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 64%;
}

.btn-group button {
  border: none;
  background: #35495e;
  color: white;
  padding: 0.5rem 2rem;
  cursor: pointer;
  margin-right: 0.5rem;
}
</style>
