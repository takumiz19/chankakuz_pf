<template>
  <div>
    <h1 class="p-hero">
      <p>chan_kaku's</p>
      <p>portfolio</p>
    </h1>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'Hero',
  data() {
    return {
      erasable: false
    }
  }
})
</script>

<style lang="scss">
.p-hero {
  padding-top: 10%;
  padding-bottom: 10%;
  background-color: #ffffff;
}
</style>
