<template>
  <div class="p-skills">
    <h1>Skills</h1>
    <div class="p-skills__items">
      <h2 class="p-slills__label">ServerSide</h2>
      <div class="p-skills__items-server">
        <div class="c-skills__item">
          <p>
            Java: 2years
          </p>
          <img src="java.png" />
        </div>
        <div class="c-skills__item">
          <p>
            Kotlin: 1.5years
          </p>
          <img src="kotlin.png" />
        </div>
        <div class="c-skills__item">
          <p>
            Scala:
            {{ calculateUsedTerm('2020-02-21T00:00:00.000Z', 'month') }}months
          </p>
          <img src="scala.png" />
        </div>
        <div class="c-skills__item">
          <p>
            Spring Framework: 2years
          </p>
          <img src="spring.png" />
        </div>
        <div class="c-skills__item">
          <p>
            Play Framework:
            {{ calculateUsedTerm('2020-02-21T00:00:00.000Z', 'month') }}months
          </p>
          <img src="play.png" />
        </div>
      </div>
      <h2 class="p-slills__label">FrontEnd</h2>
      <div class="p-skills__items-front">
        <div class="c-skills__item">
          <p>
            Vue.js:
            {{ calculateUsedTerm('2018-04-01T00:00:00.000Z', 'year') }}years
          </p>
          <img src="vue.png" />
        </div>
        <div class="c-skills__item">
          <p>
            JavaScript:
            {{ calculateUsedTerm('2018-04-01T00:00:00.000Z', 'year') }}years
          </p>
          <img src="javascript.png" />
        </div>
        <div class="c-skills__item">
          <p>
            TypeScript:
            {{ calculateUsedTerm('2020-02-21T00:00:00.000Z', 'month') }}months
          </p>
          <img src="typescript.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="js">
import Vue from 'vue'

export default Vue.extend({
  name: 'Skills',
  methods: {
    calculateUsedTerm(fromDay, format) {
      const now = this.$dayjs()
      return now.diff(this.$dayjs(fromDay), format)
    }
  }
})
</script>

<style lang="scss" scoped>
.p-skills {
  padding-top: 10%;
  padding-bottom: 10%;
  width: 100%;
  background-color: #ffffff;
  color: #000000;

  &__items-server {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    justify-content: center;
    text-align: center;
    padding-top: 20px;
  }
  &__items-front {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    text-align: center;
    padding-top: 20px;
  }
  &__label {
    padding-top: 50px;
    padding-bottom: 50px;
  }
  .c-skills__item {
    padding-left: 50px;
    padding-right: 50px;
  }
}
</style>
