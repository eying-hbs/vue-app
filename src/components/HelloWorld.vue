<template>
<div>
<h2>Hello from HelloWorld Component!</h2>
<button @click="fetchMessage">Fetch Message</button> <p v-if="message">{{ message }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: '',
    };
}, methods: {
    async fetchMessage() {
      try {
        const response = await fetch('/api/');
        this.message = await response.text();
      } catch (error) {
console.error('Error fetching message:', error); }
}, },
}; </script>
