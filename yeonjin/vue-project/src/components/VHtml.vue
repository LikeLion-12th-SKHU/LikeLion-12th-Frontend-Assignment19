<script setup>
const htmlContent = "<strong>이 텍스트는 v-html 지시자를 사용해서 쓴거에요.</strong>";
</script>

<template>
  <div>
    <p v-html="htmlContent"></p>
  </div>
</template>

<style scoped>
p {
  color: #5b65c8;
  font-size: 16px;
}
</style>
