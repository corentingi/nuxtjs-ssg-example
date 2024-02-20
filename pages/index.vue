<script setup>
import { ref } from 'vue';

const form = ref({
  name: '',
  phone: '',
  email: ''
});

const submitForm = () => {
  $fetch('/api/contact', {
    method: 'POST',
    body: JSON.stringify(form.value)
  });
  // Here you can handle form submission
  // For example, send this data to your server
};
</script>

<template>
  <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100 py-2">
    <div class="p-6 max-w-sm w-full bg-white shadow-md rounded-md">
      <div class="flex justify-center items-center">
        <span class="text-gray-700 font-semibold">Contact Form</span>
        <NuxtLink to="/contact">
          <a class="text-blue-500 ml-2">Go to contact page</a>
        </NuxtLink>
      </div>
      <form @submit.prevent="submitForm">
        <div class="mt-4">
          <label class="block text-gray-600" for="name">Name</label>
          <input class="form-input mt-1 block w-full rounded-md bg-gray-100 border-transparent focus:border-gray-500 focus:bg-white focus:ring-0" type="text" v-model="form.name" required>
        </div>
        <div class="mt-4">
          <label class="block text-gray-600" for="phone">Phone</label>
          <input class="form-input mt-1 block w-full rounded-md bg-gray-100 border-transparent focus:border-gray-500 focus:bg-white focus:ring-0" type="tel" v-model="form.phone" required>
        </div>
        <div class="mt-4">
          <label class="block text-gray-600" for="email">Email</label>
          <input class="form-input mt-1 block w-full rounded-md bg-gray-100 border-transparent focus:border-gray-500 focus:bg-white focus:ring-0" type="email" v-model="form.email" required>
        </div>
        <div class="mt-6">
          <button type="submit" class="py-2 px-4 text-center bg-blue-600 rounded-md w-full text-white hover:bg-blue-500 focus:outline-none">
            Submit
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

