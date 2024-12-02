<script setup>
import { ref } from "vue";

const showMessage = ref(false);

const toggleMessage = () => {
  showMessage.value = !showMessage.value;
};
</script>

<template>
  <div>
    <button v-on:click="toggleMessage">눌러봐요</button>
    <p v-if="showMessage">하이 v-on 실습이에요</p>
  </div>
</template>

<style scoped>
button {
  padding: 10px 20px;
  background-color: #304a6e;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #9d4ff5;
}
</style>
