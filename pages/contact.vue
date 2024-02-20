<template>
  <div class="container mx-auto">
    <h1 class="text-2xl font-bold mb-4">Contact Page</h1>
    <form>
      <div class="mb-4">
        <label for="name" class="block text-gray-700">Name</label>
        <input type="text" id="name" v-model="name" class="border border-gray-300 px-4 py-2 rounded-md w-full" />
      </div>
      <div class="mb-4">
        <label for="email" class="block text-gray-700">Email</label>
        <input type="email" id="email" v-model="email" class="border border-gray-300 px-4 py-2 rounded-md w-full" />
      </div>
      <div class="mb-4">
        <label for="message" class="block text-gray-700">Message</label>
        <textarea id="message" v-model="message" class="border border-gray-300 px-4 py-2 rounded-md w-full"></textarea>
      </div>
      <button type="submit" class="bg-blue-500 text-white px-4 py-2 rounded-md">Submit</button>
    </form>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const name = ref('');
const email = ref('');
const message = ref('');

// Add your logic here

</script>

<style>
/* Add your custom styles here */
</style>
