<script setup lang="ts">
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const loading = ref(false)
const errorMessage = ref('')

const submit = () => {
  errorMessage.value = ''

  if (!email.value || !password.value) {
    errorMessage.value = 'Email and password are required.'
    return
  }

  loading.value = true

  setTimeout(() => {
    loading.value = false
    alert(`Login attempted with ${email.value}`)
  }, 600)
}
</script>

<template>
  <form class="login-form" @submit.prevent="submit">
    <h1>Login</h1>

    <p v-if="errorMessage" class="error">{{ errorMessage }}</p>

    <label>
      Email
      <input type="email" v-model="email" placeholder="you@example.com" />
    </label>

    <label>
      Password
      <input type="password" v-model="password" placeholder="Enter password" />
    </label>

    <button type="submit" :disabled="loading">
      {{ loading ? 'Signing in...' : 'Sign in' }}
    </button>
  </form>
</template>

<style scoped>
.login-form {
  width: min(380px, 100%);
  background: white;
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 16px 40px rgba(15, 23, 42, 0.12);
  display: grid;
  gap: 1rem;
}

.login-form h1 {
  margin: 0;
  font-size: 1.6rem;
  text-align: center;
}

.login-form label {
  display: grid;
  gap: 0.5rem;
  font-weight: 600;
  color: #334155;
}

.login-form input {
  width: 100%;
  padding: 0.9rem 1rem;
  border: 1px solid #cbd5e1;
  border-radius: 0.75rem;
  font-size: 1rem;
}

.login-form button {
  width: 100%;
  padding: 0.95rem 1rem;
  border: none;
  border-radius: 0.75rem;
  background: #3b82f6;
  color: white;
  font-size: 1rem;
  cursor: pointer;
}

.login-form button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.error {
  color: #dc2626;
  font-size: 0.95rem;
}
</style>
