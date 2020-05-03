<template>
  <div class="p-profile">
    <h1>Who</h1>
    <h1 class="p-profile__name">chan_kaku</h1>
    <img src="myImage.jpg" />
    <p>Job: Software Engineer(ServerSide & FrontEnd)</p>
    <p>Hobby: Music, Game, Programming</p>
    <img class="p-profile__img" src="code_review.svg" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'Profile'
})
</script>

<style lang="scss">
.p-profile {
  padding-top: 10%;
  padding-bottom: 10%;
  background-color: #000000;
  color: #ffffff;

  &__img {
    width: 20%;
    float: left;
    @include sp {
      display: none;
    }
  }
}
</style>
