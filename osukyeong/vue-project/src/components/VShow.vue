<!-- VShowMouseTracker.vue -->
<script setup>
import { ref } from "vue";

const isMouseVisible = ref(true);
const mousePosition = ref({ x: 0, y: 0 });

const updateMousePosition = (event) => {
  mousePosition.value = { x: event.clientX, y: event.clientY };
};

window.addEventListener("mousemove", updateMousePosition);
</script>

<template>
  <div class="tracker-container">
    <button @click="isMouseVisible = !isMouseVisible" class="btn-toggle">
      마우스 추적 끄기/키기
    </button>
    <div v-show="isMouseVisible" :style="{ top: mousePosition.y + 'px', left: mousePosition.x + 'px' }" class="mouse-tracker"></div>
  </div>
</template>

<style scoped>
.tracker-container {
  position: relative;
  height: 500px;
  width: 100%;
  text-align: center;
}

.btn-toggle {
  padding: 10px 20px;
  background-color: #f59e0b;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn-toggle:hover {
  background-color: #d97706;
}

.mouse-tracker {
  position: absolute;
  width: 30px;
  height: 30px;
  background-color: rgba(0, 123, 255, 0.6);
  border-radius: 50%;
  pointer-events: none;
  transition: transform 0.1s ease-in-out;
}
</style>
