<template>
  <div>
    <vue-typer
      class="vue-typer"
      text="Hello World! I am chankaku!"
      :repeat="0"
      @completed="onComplete"
    ></vue-typer>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'Opening',
  data() {
    return {
      erasable: false
    }
  },
  methods: {
    async onComplete() {
      await setTimeout(() => {
        this.$emit('finishOpening')
      }, 2000)
    }
  }
})
</script>

<style lang="scss">
.vue-typer {
  font-size: 1.5rem;
}
</style>
