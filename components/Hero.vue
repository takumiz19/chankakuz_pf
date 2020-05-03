<template>
  <div class="p-hero">
    <h1>
      <p>chan_kaku's</p>
      <p>portfolio</p>
    </h1>
    <img src="mobile_messages.svg" />
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

<style lang="scss" scoped>
.p-hero {
  padding-top: 10%;
  padding-bottom: 10%;
  background-color: #ffffff;

  img {
    width: 20%;
    float: right;
    @include sp {
      display: none;
    }
  }
}
</style>
