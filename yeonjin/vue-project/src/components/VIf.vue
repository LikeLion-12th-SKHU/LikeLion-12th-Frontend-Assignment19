<script setup>
import { ref } from "vue";

const showMessage = ref(true);
</script>

<template>
  <div>
    <button @click="showMessage = !showMessage">
      {{ showMessage ? "숨기기" : "보이기" }}
    </button>
    <div>
      <p v-if="showMessage">보이기 누르면 이 텍스트 보이기</p>
      <p v-else>숨기기 누르면 이 텍스트 보이기</p>
    </div>
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

p {
  font-size: 16px;
  color: #333;
}

p:nth-child(1) {
  color:  #000000;
}


</style>
