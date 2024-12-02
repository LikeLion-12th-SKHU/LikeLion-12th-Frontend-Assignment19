<script setup>
const items = ["다들 12기 멋사 너무 수고했어요", "효중님 조지미 너무 수고하셨어요! 감사해요! S2", "예은님 1년동안 함께 해서 너무 좋았어요~! "];
</script>

<template>
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ index + 1 }}. {{ item }}
    </li>
  </ul>
</template>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin: 5px 0;
  padding: 5px;
  background-color: #f9f9f9;
  border: 1px solid #ddd;
}
</style>
