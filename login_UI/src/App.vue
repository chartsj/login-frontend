<script setup lang="ts">
import LoginForm from './components/LoginForm.vue'
</script>

<template>
  <div id="app">
    <LoginForm />
  </div>
</template>

<style scoped>
#app {
  min-height: 100vh;
  display: grid;
  place-items: center;
  padding: 2rem;
  background: #f0f4f8;
}
</style>
