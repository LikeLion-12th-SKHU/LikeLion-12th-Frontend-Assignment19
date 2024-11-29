<script setup>
import { ref } from "vue";

const isRed = ref(true);
</script>

<template>
  <div>
    <p v-show="isRed">보이거나 숨길 수 있습니당</p>
    <button @click="isRed = !isRed">표시/숨기기</button>
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
