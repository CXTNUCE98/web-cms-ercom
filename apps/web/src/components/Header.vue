<script setup lang="ts">
import { ref } from 'vue';

const mobileMenuOpen = ref(false);
</script>

<template>
  <header class="bg-white border-b border-gray-200">
    <div class="container mx-auto px-4 py-4">
      <div class="flex items-center justify-between">
        <!-- Logo -->
        <div class="flex items-center space-x-2">
          <div class="w-8 h-8 bg-primary rounded-full flex items-center justify-center">
            <span class="text-white font-bold text-lg">C</span>
          </div>
          <span class="text-xl font-semibold text-gray-900">Clothing.</span>
        </div>

        <!-- Desktop Navigation -->
        <nav class="hidden lg:flex items-center space-x-8">
          <a href="#" class="text-gray-700 hover:text-primary transition">Home</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">Shop</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">Women</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">Men</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">Accessories</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">About Us</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">Contact Us</a>
          <a href="#" class="text-gray-700 hover:text-primary transition">Blog</a>
        </nav>

        <!-- Icons -->
        <div class="flex items-center space-x-4">
          <!-- Search Icon -->
          <button class="text-gray-700 hover:text-primary transition">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
          </button>
          
          <!-- Wishlist Icon -->
          <button class="text-gray-700 hover:text-primary transition">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
            </svg>
          </button>
          
          <!-- Cart Icon -->
          <button class="text-gray-700 hover:text-primary transition relative">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
            </svg>
          </button>
          
          <!-- User Icon -->
          <button class="text-gray-700 hover:text-primary transition">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
            </svg>
          </button>

          <!-- Mobile Menu Button -->
          <button @click="mobileMenuOpen = !mobileMenuOpen" class="lg:hidden text-gray-700">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Menu -->
      <nav v-if="mobileMenuOpen" class="lg:hidden mt-4 pb-4 space-y-2">
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Home</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Shop</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Women</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Men</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Accessories</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">About Us</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Contact Us</a>
        <a href="#" class="block text-gray-700 hover:text-primary transition py-2">Blog</a>
      </nav>
    </div>
  </header>
</template>

