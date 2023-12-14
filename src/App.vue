<template>
  <v-app>
    <v-main>
      <Quiz quiz_text="quiz_test1" />
      <Quiz quiz_text="quiz_test2" />
      <Quiz quiz_text="quiz_test3" />
    </v-main>
  </v-app>
</template>

<script>
import Quiz from './components/Quiz.vue'

export default {
  name: 'App',
  components: {
    Quiz
  }
}
</script>
