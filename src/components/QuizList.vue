<template>
  <div class="quiz-list">
    <div class="tab" v-bind:class="{active: currentTab === 0}">
      <h3>What is a framework?</h3>
      <ul>
        <li>An intelligent art</li>
        <li>A framework is a work of frame</li>
        <li>A work built on a frame</li>
      </ul>
    </div>
    <div class="tab" v-bind:class="{active: currentTab === 1}">
      <h3>Who is Arya Stark?</h3>
      <ul>
        <li>A girl has no name</li>
        <li>The lady of Winterfell</li>
        <li>A fullstack developer</li>
      </ul>
    </div>
    <div class="tab" v-bind:class="{active: currentTab === 2}">
      <h3>Coding is next to?</h3>
      <ul>
        <li>Rugby</li>
        <li>Buisness</li>
        <li>Skating</li>
      </ul>
    </div>
    <div class="tab" v-bind:class="{active: currentTab === 3}">
      <h3>A senior developer is known as?</h3>
      <ul>
        <li>Senior Dev</li>
        <li>Senior citizen of a company or</li>
        <li>Team Lead</li>
      </ul>
    </div>
    <div class="tab" v-bind:class="{active: currentTab === 4}">
      <h3>UI/UX is terminology for?</h3>
      <ul>
        <li>Sign Language</li>
        <li>Mobile Applications</li>
        <li>Extended Reality</li>
      </ul>
    </div>

    <div style="overflow:auto;">
      <div style="float:right;">
        <button type="button" v-show="currentTab > 0" v-on:click="currentTab--">Previous</button>
        <button type="button" v-on:click="nextQuiz" v-show="currentTab <= 3">Next</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "QuizList",
  data() {
    return {
      currentTab: 0,
      tab: true,
      active: true,
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
          answer: "A girl has no name"
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
  },
  methods: {
    nextQuiz: function(currentTab) {
      if (this.currentTab >= 4) return;
      this.currentTab++;
    }
  }
};
</script>

<style scoped>
.tab {
  display: none;
}

.tab.active {
  display: block;
}

.tab h3 {
  color: #d6ffe9;
  font-size: 2em;
  padding: 0.4em 0.5em;
  border-left: 5px solid #237949;
  background: #7ef0ce71;
  margin-bottom: 0.2em;
}
.quiz-list ul {
  list-style-type: none;
}
.quiz-list li {
  background: rgb(142, 243, 186);
  padding: 1rem;
  margin-bottom: 0.5rem;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}

.quiz-list li:hover {
  opacity: 0.7;
  margin-left: 0.4em;
}

button {
  border: none;
  background: #35495e;
  color: white;
  padding: 0.5rem 2rem;
  cursor: pointer;
  margin-right: 0.5rem;
}
</style>
