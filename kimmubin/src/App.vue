<script setup>
// import VModel from "./components/VModel.vue";
// import VOnClick from "./components/VOnClick.vue";
// import VBind from "./components/VBind.vue";
import VIf from "./components/VIf.vue";
import VShow from "./components/VShow.vue";
import VFor from "./components/VFor.vue";
</script>

<template>
  <main>
    <h2>Vue.js 실습</h2>
    <section>
      <h3>v-if 과제 1</h3>
      <VIf />
    </section>
    <section>
      <h3>v-show 과제 2</h3>
      <VShow />
    </section>
    <section>
      <h3>v-for 과제 3</h3>
      <VFor />
    </section>
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
