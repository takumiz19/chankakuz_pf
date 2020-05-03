<template>
  <div class="p-sns">
    <div class="p-sns__items">
      <h2 class="p-sns__label">SNS</h2>
      <div class="p-sns__items-sns">
        <div class="c-sns__item">
          <a href="https://twitter.com/chan_kakuz"><p>Twitter</p></a>
          <!-- <img src="twitter.png" /> -->
        </div>
        <div class="c-sns__item">
          <a href="https://qiita.com/chan_kaku"><p>Qiita</p></a>
          <!-- <img src="qiita.png" /> -->
        </div>
        <div class="c-sns__item">
          <a href="https://github.com/takumiz19"><p>GitHub</p></a>
          <!-- <img src="github.png" /> -->
        </div>
      </div>
      <h2 class="p-sns__label">Slide</h2>
      <div class="p-sns__items-slides">
        <div class="c-sns__item">
          <a href="https://slides.com/chan_kakuz"><p>Slides</p></a>
          <!-- <img src="slides.png" /> -->
        </div>
        <div class="c-sns__item">
          <a href="https://speakerdeck.com/takumiz19"><p>SpeakerDeck</p></a>
          <!-- <img src="speakerdeck.png" /> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'Sns'
})
</script>

<style lang="scss">
.p-sns {
  padding-top: 10%;
  padding-bottom: 10%;
  background-color: #000000;
  color: #ffffff;

  &__items-sns {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    text-align: center;
    padding-top: 20px;
    @include sp {
      padding-top: 0px;
    }
  }
  &__items-slides {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    text-align: center;
    padding-top: 20px;
    @include sp {
      padding-top: 0;
    }
  }
  &__label {
    padding-top: 50px;
    padding-bottom: 50px;
    @include sp {
      padding-top: 20px;
      padding-bottom: 20px;
    }
  }
  .c-sns__item {
    padding-left: 50px;
    padding-right: 50px;
  }
}
</style>
