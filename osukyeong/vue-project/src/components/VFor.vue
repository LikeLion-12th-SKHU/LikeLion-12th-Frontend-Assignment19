<!-- VForRandomImage.vue -->
<script setup>
import { ref } from "vue";

const images = ref([]);
const addRandomImage = () => {
  const randomNumber = Math.floor(Math.random() * 1000);
  const randomImageUrl = `https://picsum.photos/200/300?random=${randomNumber}`;
  images.value.push(randomImageUrl);
};
</script>

<template>
  <div class="image-gallery">
    <button @click="addRandomImage" class="btn-add-image">랜덤 이미지 추가</button>
    <div class="gallery">
      <img v-for="(image, index) in images" :key="index" :src="image" class="gallery-image" />
    </div>
  </div>
</template>

<style scoped>
.image-gallery {
  text-align: center;
  margin-top: 50px;
}

.btn-add-image {
  padding: 10px 20px;
  background-color: #10b981;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn-add-image:hover {
  background-color: #059669;
}

.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  margin-top: 20px;
}

.gallery-image {
  width: 200px;
  height: 300px;
  object-fit: cover;
  border-radius: 10px;
  transition: transform 0.3s;
}

.gallery-image:hover {
  transform: scale(1.1);
}
</style>
