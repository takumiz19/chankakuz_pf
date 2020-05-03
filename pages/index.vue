<template>
  <div class="container">
    <opening
      v-if="!finished"
      class="l-opening"
      @finishOpening="finishOpening"
    ></opening>
    <transition name="fade">
      <hero v-if="finished"></hero>
    </transition>
    <transition name="fade">
      <profile v-if="finished"></profile>
    </transition>
    <transition name="fade">
      <skills v-if="finished"></skills>
    </transition>
    <transition name="fade">
      <sns v-if="finished"></sns>
    </transition>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Opening from '~/components/Opening.vue'
import Hero from '~/components/Hero.vue'
import Profile from '~/components/Profile.vue'
import Skills from '~/components/Skills.vue'
import Sns from '~/components/Sns.vue'

export default Vue.extend({
  components: {
    Opening,
    Hero,
    Profile,
    Skills,
    Sns
  },
  data() {
    return {
      finished: false
    }
  },
  methods: {
    finishOpening() {
      this.finished = true
    }
  }
})
</script>

<style lang="scss">
.container {
  margin: 0 auto;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.l-opening {
  padding-top: 25%;
  // padding-bottom: 50%;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
