<template>
  <v-app>
    <v-main class="d-flex">
      <div>
        <transition name="transit" v-on:after-enter="onClickOK">
          <p v-if="flgOK" class="text-red text-h1 trans mx-10">〇</p>
        </transition>
        <transition name="transit" v-on:after-enter="onClickNG">
          <p v-if="flgNG" class="text-blue text-h1 trans mx-10 -mt-20">×</p>
        </transition>
      </div>
      <v-container class="d-flex flex-wrap w-75 justify-center" width="1000">
        <Quiz title="A" quiz_text="quiz_test1" class="text-pink" v-on:click="onClickNG" />
        <Quiz title="B" quiz_text="quiz_test2" class="text-lime" v-on:click="onClickNG" />
        <Quiz title="C" quiz_text="quiz_test3" class="text-teal" v-on:click="onClickOK" />
        <Quiz title="D" quiz_text="quiz_test3" class="text-cyan" v-on:click="onClickNG" />
      </v-container>
      <div>
        <transition name="transit" v-on:after-enter="onClickOK">
          <p v-if="flgOK" class="text-red text-h1 trans mx-10">〇</p>
        </transition>
        <transition name="transit" v-on:after-enter="onClickNG">
          <p v-if="flgNG" class="text-blue text-h1 trans mx-10 -mt-20">×</p>
        </transition>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import Quiz from './components/Quiz.vue'

export default {
  name: 'App',
  components: {
    Quiz
  },
  data() {
    return {
      flgOK: false,
      flgNG: false
    }
  },
  methods: {
    onClickOK() {
      this.flgOK = !this.flgOK
    },
    onClickNG() {
      this.flgNG = !this.flgNG
    }
  }
}
</script>
<style>
.trans {
  position: relative;
  z-index: 100;
}

.transit-enter-active {
  transition: 0.1s;
}

.transit-leave-active {
  transition: 2s;
}

.transit-enter,
.transit-leave-to {
  transform: translateY(500px)
}
</style>
