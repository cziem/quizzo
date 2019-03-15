<template>
  <div class="quiz-list">
    <ul>
      <li :key="quiz.id" v-for="quiz in quizList">{{ quiz.question }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "QuizList",
  data() {
    return {
      quizList: [
        {
          question: "What is a framework?",
          id: 1,
          isCorrect: false,
          answer: "A framework is a work of frame"
        },
        {
          question: "Who is Arya Stark?",
          id: 2,
          isCorrect: false,
          answer: "A stack of cards"
        },
        {
          question: "Coding is next to?",
          id: 3,
          isCorrect: false,
          answer: "Skating"
        },
        {
          question: "A senior developer is known as?",
          id: 4,
          isCorrect: false,
          answer: "Team Lead"
        },
        {
          question: "UI/UX is terminology for?",
          id: 5,
          isCorrect: false,
          answer: "Sign Language"
        }
      ]
    };
  }
};
</script>

<style scoped>
.quiz-list ul {
  list-style-type: none;
}
.quiz-list li {
  background: rgb(142, 243, 186);
  padding: 1rem;
  margin-bottom: 0.5rem;
  border-left: 5px solid #237949;
}
</style>
