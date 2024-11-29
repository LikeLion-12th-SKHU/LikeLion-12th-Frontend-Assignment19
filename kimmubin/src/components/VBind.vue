<script setup>
import { ref } from "vue";

const isRed = ref(true);
</script>

<template>
  <div>
    <p v-bind:style="{ color: isRed ? 'red' : 'blue' }">
      색이 바뀌는 신기한 텍스트
    </p>
    <button v-on:click="isRed = !isRed">색상 변경</button>
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
