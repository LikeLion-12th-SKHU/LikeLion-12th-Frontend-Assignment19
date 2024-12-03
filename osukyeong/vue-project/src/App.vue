<script setup>
import VModel from "./components/VModel.vue";
import VOnClick from "./components/VOnClick.vue";
import VBind from "./components/VBind.vue";
import VElse from "./components/VElse.vue";
import VFor from "./components/VFor.vue";
import VShow from "./components/VShow.vue";
</script>

<template>
  <main>

      <h1>📖 강의</h1>
    <section>
    </section>

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

      <h1>💡 과제</h1>
    <section>
    </section>

    <!-- v-else 실습 -->
    <section>
      <h3>v-else 실습</h3>
       <VElse />
    </section>
    <br />

    <!-- v-for 실습 -->
    <section>
      <h3>v-for 실습</h3>
      <VFor />
    </section>
    <br />

    <!-- v-show 실습 -->
    <section>
      <h3>v-show 실습</h3>
       <VShow />
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
</style>
