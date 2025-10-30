<script setup lang="ts">
</script>

<template>
  <!-- Limited Time Offers Section -->
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Left Content -->
        <div class="space-y-8">
          <div>
            <p class="text-sm text-gray-500 mb-2">Limited Time Offers</p>
            <h2 class="text-4xl lg:text-5xl font-bold text-gray-900 mb-6">
              25% Off All Fashion Favorites - Limited Time!
            </h2>
            <p class="text-lg text-gray-600 max-w-lg">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
            </p>
          </div>
          
          <button class="bg-primary text-white px-8 py-4 rounded-lg font-semibold hover:bg-primary/90 transition flex items-center space-x-2">
            <span>Shop Now</span>
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </button>
        </div>
        
        <!-- Right Content - Image -->
        <div class="relative">
          <img 
            src="https://images.unsplash.com/photo-1496747611176-843222e1e57c?w=600&h=700&fit=crop" 
            alt="Fashion Models" 
            class="w-full h-[500px] object-cover rounded-lg shadow-2xl"
          >
        </div>
      </div>
    </div>
  </section>

  <!-- Deals of the Day Section -->
  <section class="py-16 bg-gray-50">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <p class="text-sm text-gray-500 mb-2">Today Deals</p>
        <h2 class="text-4xl font-bold text-gray-900 mb-6">Deals of the Day</h2>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto">
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam
        </p>
      </div>
      
      <!-- Deals Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Deal Card 1 -->
        <div class="bg-white rounded-lg shadow-sm hover:shadow-lg transition group">
          <div class="relative">
            <img 
              src="https://images.unsplash.com/photo-1594633312681-425c7b97ccd1?w=400&h=500&fit=crop" 
              alt="Stylist Dress"
              class="w-full h-80 object-cover rounded-t-lg"
            >
            
            <!-- Discount Badge -->
            <div class="absolute top-4 left-4 bg-green-500 text-white px-3 py-1 rounded-full text-sm font-medium">
              50% off
            </div>
            
            <!-- Action Icons -->
            <div class="absolute top-4 right-4 space-y-2 opacity-0 group-hover:opacity-100 transition">
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                </svg>
              </button>
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 8V4m0 0h4M4 4l5 5m11-1V4m0 0h-4m4 0l-5 5M4 16v4m0 0h4m-4 0l5-5m11 5l-5-5m5 5v-4m0 4h-4" />
                </svg>
              </button>
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
              </button>
            </div>
          </div>
          
          <div class="p-6">
            <div class="text-sm text-gray-500 mb-2">Dress</div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Stylist Dress</h3>
            
            <!-- Rating -->
            <div class="flex items-center space-x-1 mb-4">
              <div class="flex text-yellow-400">
                <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 fill-current" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
              </div>
              <span class="text-sm text-gray-600 ml-2">4.8</span>
            </div>
            
            <!-- Price -->
            <div class="flex items-center space-x-2 mb-4">
              <span class="text-2xl font-bold text-gray-900">$75.00</span>
              <span class="text-lg text-gray-500 line-through">$150.00</span>
            </div>
            
            <!-- Description -->
            <p class="text-gray-600 text-sm mb-4">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
            </p>
            
            <!-- Shop Now Button -->
            <button class="w-full text-primary py-3 rounded-lg font-medium hover:bg-primary hover:text-white transition border border-primary">
              Shop Now →
            </button>
          </div>
        </div>

        <!-- Deal Card 2 -->
        <div class="bg-white rounded-lg shadow-sm hover:shadow-lg transition group">
          <div class="relative">
            <img 
              src="https://images.unsplash.com/photo-1515372039744-b8f02a3ae446?w=400&h=500&fit=crop" 
              alt="Modern Party Dress"
              class="w-full h-80 object-cover rounded-t-lg"
            >
            
            <!-- Discount Badge -->
            <div class="absolute top-4 left-4 bg-green-500 text-white px-3 py-1 rounded-full text-sm font-medium">
              20% off
            </div>
            
            <!-- Action Icons -->
            <div class="absolute top-4 right-4 space-y-2 opacity-0 group-hover:opacity-100 transition">
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                </svg>
              </button>
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 8V4m0 0h4M4 4l5 5m11-1V4m0 0h-4m4 0l-5 5M4 16v4m0 0h4m-4 0l5-5m11 5l-5-5m5 5v-4m0 4h-4" />
                </svg>
              </button>
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
              </button>
            </div>
          </div>
          
          <div class="p-6">
            <div class="text-sm text-gray-500 mb-2">Dress</div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Modern Party Dress</h3>
            
            <!-- Rating -->
            <div class="flex items-center space-x-1 mb-4">
              <div class="flex text-yellow-400">
                <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 fill-current" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
              </div>
              <span class="text-sm text-gray-600 ml-2">4.9</span>
            </div>
            
            <!-- Price -->
            <div class="flex items-center space-x-2 mb-4">
              <span class="text-2xl font-bold text-gray-900">$80.00</span>
              <span class="text-lg text-gray-500 line-through">$100.00</span>
            </div>
            
            <!-- Description -->
            <p class="text-gray-600 text-sm mb-4">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
            </p>
            
            <!-- Shop Now Button -->
            <button class="w-full text-primary py-3 rounded-lg font-medium hover:bg-primary hover:text-white transition border border-primary">
              Shop Now →
            </button>
          </div>
        </div>

        <!-- Deal Card 3 -->
        <div class="bg-white rounded-lg shadow-sm hover:shadow-lg transition group">
          <div class="relative">
            <img 
              src="https://images.unsplash.com/photo-1591047139829-d91aecb6caea?w=400&h=500&fit=crop" 
              alt="Fashion Item"
              class="w-full h-80 object-cover rounded-t-lg"
            >
            
            <!-- Discount Badge -->
            <div class="absolute top-4 left-4 bg-green-500 text-white px-3 py-1 rounded-full text-sm font-medium">
              25% off
            </div>
            
            <!-- Action Icons -->
            <div class="absolute top-4 right-4 space-y-2 opacity-0 group-hover:opacity-100 transition">
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                </svg>
              </button>
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 8V4m0 0h4M4 4l5 5m11-1V4m0 0h-4m4 0l-5 5M4 16v4m0 0h4m-4 0l5-5m11 5l-5-5m5 5v-4m0 4h-4" />
                </svg>
              </button>
              <button class="w-10 h-10 bg-white rounded-full flex items-center justify-center shadow-md hover:bg-primary hover:text-white transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
              </button>
            </div>
          </div>
          
          <div class="p-6">
            <div class="text-sm text-gray-500 mb-2">Fashion</div>
            <h3 class="text-xl font-semibold text-gray-900 mb-2">Trendy Fashion Item</h3>
            
            <!-- Rating -->
            <div class="flex items-center space-x-1 mb-4">
              <div class="flex text-yellow-400">
                <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 fill-current" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
              </div>
              <span class="text-sm text-gray-600 ml-2">4.7</span>
            </div>
            
            <!-- Price -->
            <div class="flex items-center space-x-2 mb-4">
              <span class="text-2xl font-bold text-gray-900">$65.00</span>
              <span class="text-lg text-gray-500 line-through">$85.00</span>
            </div>
            
            <!-- Description -->
            <p class="text-gray-600 text-sm mb-4">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
            </p>
            
            <!-- Shop Now Button -->
            <button class="w-full text-primary py-3 rounded-lg font-medium hover:bg-primary hover:text-white transition border border-primary">
              Shop Now →
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

