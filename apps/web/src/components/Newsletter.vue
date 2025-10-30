<script setup lang="ts">
import { ref } from 'vue';

const email = ref('');

const subscribe = () => {
  if (email.value) {
    alert('Thank you for subscribing!');
    email.value = '';
  }
};
</script>

<template>
  <!-- Newsletter Section -->
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <p class="text-sm text-gray-500 mb-2">Our Newsletter</p>
        <h2 class="text-4xl font-bold text-gray-900 mb-4">
          Subscribe to Our Newsletter to Get Updates to Our Latest Collection
        </h2>
        <p class="text-lg text-gray-600">
          Get 20% off on your first order just by subscribing to our newsletter
        </p>
      </div>
      
      <!-- Newsletter Form -->
      <div class="max-w-md mx-auto">
        <form @submit.prevent="subscribe" class="flex">
          <div class="flex-1 relative">
            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
              <div class="w-8 h-8 bg-secondary rounded flex items-center justify-center">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 text-primary" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
            </div>
            <input 
              v-model="email"
              type="email" 
              placeholder="Enter Email Address"
              class="w-full pl-12 pr-4 py-4 border border-gray-300 rounded-l-lg focus:outline-none focus:ring-2 focus:ring-primary focus:border-transparent"
              required
            >
          </div>
          <button 
            type="submit"
            class="bg-primary text-white px-8 py-4 rounded-r-lg font-semibold hover:bg-primary/90 transition"
          >
            Subscribe
          </button>
        </form>
      </div>
    </div>
  </section>
</template>

