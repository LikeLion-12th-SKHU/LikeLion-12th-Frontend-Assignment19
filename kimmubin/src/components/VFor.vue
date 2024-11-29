<script setup>
const example = ["순서대로 출력", "index[0]", "index[1]", "index[2]"];
</script>

<template>
  <ul>
    <li v-for="(name, index) in example" :key="index">
      {{ name }}
    </li>
  </ul>
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
