<script setup>
import { ref } from "vue";

const message = ref("V-model 코드에서 입력한 메세지");
</script>

<template>
  <div>
    <input
      v-model="message"
      placeholder="메시지를 입력하세요"
      class="input-box"
    />
    <p>(( message ))</p>
  </div>
</template>

<style scoped>
.input-box {
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;

}
</style>
