<script setup>
import { ref } from "vue";
const isRed = ref(true);
</script>

<template>
  <div>
    <p v-if="isRed" style="color: red">v-if로 색이 바뀌는 텍스트</p>
    <p v-else style="color: blue">v-if로 색이 바뀌는 텍스트</p>
    <button @click="isRed = !isRed">색상 변경</button>
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
  background-color: #c0d0ef;
}
</style>
