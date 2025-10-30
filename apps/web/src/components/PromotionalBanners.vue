<script setup lang="ts">
</script>

<template>
  <!-- Promotional Banners Section -->
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        <!-- Men's Collection Banner -->
        <div class="bg-gray-50 rounded-lg p-8 lg:p-12">
          <div class="flex flex-col lg:flex-row items-center gap-8">
            <div class="flex-1 space-y-6">
              <div>
                <p class="text-sm text-gray-500 mb-2">Flat 20% Discount</p>
                <h2 class="text-3xl lg:text-4xl font-bold text-gray-900 mb-4">Men's Latest Collection</h2>
                <p class="text-gray-600">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                </p>
              </div>
              
              <button class="bg-orange-500 text-white px-6 py-3 rounded-lg font-semibold hover:bg-orange-600 transition flex items-center space-x-2">
                <span>Shop Now</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                </svg>
              </button>
            </div>
            
            <div class="flex-shrink-0">
              <img 
                src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=300&h=400&fit=crop" 
                alt="Men's Fashion"
                class="w-64 h-80 object-cover rounded-lg shadow-lg"
              >
            </div>
          </div>
        </div>

        <!-- Women's Fashion Banner -->
        <div class="bg-orange-500 rounded-lg p-8 lg:p-12">
          <div class="flex flex-col lg:flex-row items-center gap-8">
            <div class="flex-1 space-y-6">
              <div>
                <p class="text-sm text-white/80 mb-2">Flat 25% Discount</p>
                <h2 class="text-3xl lg:text-4xl font-bold text-white mb-4">Women's Latest Fashion</h2>
                <p class="text-white/90">
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                </p>
              </div>
              
              <button class="bg-primary text-white px-6 py-3 rounded-lg font-semibold hover:bg-primary/90 transition flex items-center space-x-2">
                <span>Shop Now</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                </svg>
              </button>
            </div>
            
            <div class="flex-shrink-0">
              <img 
                src="https://images.unsplash.com/photo-1496747611176-843222e1e57c?w=300&h=400&fit=crop" 
                alt="Women's Fashion"
                class="w-64 h-80 object-cover rounded-lg shadow-lg"
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Instagram Feed Section -->
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <p class="text-sm text-gray-500 mb-2">Follow Us</p>
        <h2 class="text-4xl font-bold text-gray-900">Follow Us On Instagram</h2>
      </div>
      
      <div class="grid grid-cols-2 md:grid-cols-5 gap-4">
        <div v-for="i in 5" :key="i" class="relative group cursor-pointer">
          <img 
            :src="`https://images.unsplash.com/photo-${1496747611176 + i}?w=300&h=300&fit=crop`" 
            :alt="`Instagram post ${i}`"
            class="w-full h-64 object-cover rounded-lg hover:scale-105 transition-transform duration-300"
          >
          <div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity rounded-lg flex items-center justify-center">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-white" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
            </svg>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

