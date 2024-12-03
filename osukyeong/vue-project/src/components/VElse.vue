<!-- VElse.vue -->
<script setup>
import { ref } from "vue";

const isLoggedIn = ref(false);
</script>

<template>
  <div class="container">
    <button @click="isLoggedIn = !isLoggedIn" :class="{ 'logged-in': isLoggedIn, 'logged-out': !isLoggedIn }">
      <span v-if="isLoggedIn">🙋‍♂️</span>
      <span v-else>🔒</span>
      {{ isLoggedIn ? '로그아웃' : '로그인' }}
    </button>
    
    <p v-if="isLoggedIn" class="message login">환영합니다! 로그인 했습니다.</p>
    <p v-else class="message logout">로그인이 필요합니다.</p>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 20vh;
  text-align: center;
}

button {
  padding: 12px 25px;
  font-size: 16px;
  background-color: #3b82f6;
  color: white;
  border: none;
  border-radius: 50px;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 8px;
  transition: transform 0.3s ease, background-color 0.3s ease;
}

button:hover {
  background-color: #2563eb;
  transform: scale(1.05);
}

button.logged-in {
  background-color: #10b981;
}

button.logged-out {
  background-color: #ef4444;
}

.message {
  font-size: 20px;
  font-weight: bold;
  margin-top: 20px;
  opacity: 0;
  transition: opacity 0.6s ease-in-out;
}

.message.login {
  color: #10b981;
  animation: slideIn 1s forwards;
}

.message.logout {
  color: #ef4444;
  animation: slideIn 1s forwards;
}

@keyframes slideIn {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
