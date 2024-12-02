<script setup>
import VModel from "./components/VModel.vue";
import VOnClick from "./components/VOnClick.vue";
import VBind from "./components/VBind.vue";
import VIf from "./components/VIf.vue";
import VFor from "./components/VFor.vue";
import VHtml from "./components/VHtml.vue";
</script>

<template>
<main>
  <h2>Vue.js 실습</h2>

  <!-- v-model 실습 -->
  <section>
    <h3>v-model 실습</h3>
    <VModel />
  </section>
  <br />

  <!-- v-on:click 실습 -->
  <section>
    <h3>v-on:click 실습</h3>
    <VOnClick />
  </section>
  <br />

  <!-- v-bind 실습 -->
  <section>
    <h3>v-bind 실습</h3>
    <VBind />
  </section>
  <br />

  <!-- v-if 실습 -->
  <section>
    <h3>v-if 실습</h3>
    <VIf />
  </section>
  <br />

  <!-- v-for 실습 -->
  <section>
    <h3>v-for 실습</h3>
    <VFor />
  </section>
  <br />

  <!-- v-html 실습 -->
  <section>
    <h3>v-html 실습</h3>
    <VHtml />
  </section>
  <br />
</main>
</template>

<style scoped>
main {
  padding: 30px;
  margin: 30px auto;
  max-width: 600px;
  border: 1px solid #ccc;
  box-shadow: 3px 3px 3px #aaa;
}

section {
  padding-bottom: 20px;
  border-bottom: 1px solid #ccc;
}

h2 {
  text-align: center;
  color: #333;
}

h3 {
  color: #555;
}
</style>
