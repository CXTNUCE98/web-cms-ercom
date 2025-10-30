<script setup lang="ts">
import { ref } from 'vue';
import LimitedTimeOffers from './LimitedTimeOffers.vue';
import PromotionalBanners from './PromotionalBanners.vue';
import TestimonialsAndBlog from './TestimonialsAndBlog.vue';
import FAQ from './FAQ.vue';
import Newsletter from './Newsletter.vue';

const activeTab = ref('All');

const features = [
  {
    icon: '📦',
    title: 'Free Shipping',
    description: 'Free shipping for order above $180'
  },
  {
    icon: '💳',
    title: 'Flexible Payment',
    description: 'Multiple secure payment options'
  },
  {
    icon: '🎧',
    title: '24x7 Support',
    description: 'We support online all days.'
  }
];

const categories = [
  {
    title: '2500+ Items',
    subtitle: "For Women's",
    items: ['Blazers', 'T-Shirts and Blouses', 'Dresses', 'Jackets & Coats', 'Jeans', 'Knit', 'Sarees'],
    image: 'https://images.unsplash.com/photo-1496747611176-843222e1e57c?w=400&h=500&fit=crop'
  },
  {
    title: '1500+ Items',
    subtitle: "For Men's",
    items: ['Blazers', 'T-Shirts and Shirts', 'Jackets & Coats', 'Jeans'],
    image: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=400&h=500&fit=crop'
  },
  {
    title: '800+ Items',
    subtitle: 'Accessories',
    items: ['Handbags', 'Watches', 'Sunglasses', 'Hat'],
    image: 'https://images.unsplash.com/photo-1553062407-98eeb64c6a62?w=400&h=500&fit=crop'
  }
];

const products = [
  {
    id: 1,
    name: 'Trendy Brown Coat',
    category: 'Coats',
    price: 75.00,
    originalPrice: 150.00,
    discount: 50,
    rating: 4.8,
    image: 'https://images.unsplash.com/photo-1591047139829-d91aecb6caea?w=300&h=400&fit=crop',
    countdown: { days: 5, hours: 12, minutes: 30, seconds: 25 }
  },
  {
    id: 2,
    name: 'Stylist Dress',
    category: 'Dress',
    price: 75.00,
    originalPrice: 150.00,
    discount: 50,
    rating: 4.8,
    image: 'https://images.unsplash.com/photo-1594633312681-425c7b97ccd1?w=300&h=400&fit=crop'
  },
  {
    id: 3,
    name: 'Modern Party Dress',
    category: 'Dress',
    price: 80.00,
    originalPrice: 100.00,
    discount: 20,
    rating: 4.9,
    image: 'https://images.unsplash.com/photo-1515372039744-b8f02a3ae446?w=300&h=400&fit=crop'
  }
];

const tabs = ['All', 'Women', 'Men', 'Accessories'];
</script>

<template>
  <div class="min-h-screen bg-white">
    <!-- Hero Section -->
    <section class="bg-gradient-to-r from-gray-50 to-white py-16">
      <div class="container mx-auto px-4">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
          <!-- Left Content -->
          <div class="space-y-8">
            <!-- Sale Banner -->
            <div class="inline-flex items-center space-x-2 bg-gray-100 px-4 py-2 rounded-full">
              <span class="text-green-600">🍃</span>
              <span class="text-sm font-medium text-gray-700">50% OFF Summer Super Sale</span>
            </div>
            
            <!-- Main Heading -->
            <h1 class="text-4xl lg:text-6xl font-bold text-gray-900 leading-tight">
              Step into Style:<br>
              <span class="text-primary">Your Ultimate Fashion Destination</span>
            </h1>
            
            <!-- Description -->
            <p class="text-lg text-gray-600 max-w-lg">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore.
            </p>
            
            <!-- CTA Button -->
            <button class="bg-primary text-white px-8 py-4 rounded-lg font-semibold hover:bg-primary/90 transition flex items-center space-x-2">
              <span>Shop Now</span>
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
              </svg>
            </button>
          </div>
          
          <!-- Right Content - Hero Image -->
          <div class="relative">
            <img 
              src="https://images.unsplash.com/photo-1496747611176-843222e1e57c?w=600&h=700&fit=crop" 
              alt="Fashion Model" 
              class="w-full h-[600px] object-cover rounded-lg shadow-2xl"
            >
            <!-- Floating Element -->
            <div class="absolute top-8 right-8 bg-white p-4 rounded-lg shadow-lg">
              <div class="flex items-center space-x-2">
                <span class="text-2xl">☀️</span>
                <div>
                  <p class="font-semibold text-sm">Summer Shades</p>
                  <p class="text-xs text-gray-500">New Collection</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="feature in features" :key="feature.title" class="text-center space-y-4">
            <div class="text-4xl">{{ feature.icon }}</div>
            <h3 class="text-xl font-semibold text-gray-900">{{ feature.title }}</h3>
            <p class="text-gray-600">{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Product Categories Section -->
    <section class="py-16 bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div v-for="category in categories" :key="category.subtitle" class="bg-white rounded-lg p-8 shadow-sm hover:shadow-md transition">
            <div class="space-y-6">
              <div>
                <h3 class="text-3xl font-bold text-gray-900">{{ category.title }}</h3>
                <h4 class="text-2xl font-semibold text-primary">{{ category.subtitle }}</h4>
              </div>
              
              <ul class="space-y-2">
                <li v-for="item in category.items" :key="item" class="text-gray-600">
                  {{ item }}
                </li>
              </ul>
              
              <img 
                :src="category.image" 
                :alt="category.subtitle"
                class="w-full h-64 object-cover rounded-lg"
              >
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Top Seller Products Section -->
    <section class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-12">
          <h2 class="text-4xl font-bold text-gray-900 mb-4">Our Products</h2>
          <p class="text-xl text-gray-600">Our Top Seller Products</p>
        </div>
        
        <!-- Filter Tabs -->
        <div class="flex justify-center mb-12">
          <div class="bg-gray-100 rounded-lg p-1">
            <button 
              v-for="tab in tabs" 
              :key="tab"
              @click="activeTab = tab"
              :class="[
                'px-6 py-3 rounded-md font-medium transition',
                activeTab === tab 
                  ? 'bg-primary text-white' 
                  : 'text-gray-700 hover:text-primary'
              ]"
            >
              {{ tab }}
            </button>
          </div>
        </div>
        
        <!-- Products Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <div v-for="product in products" :key="product.id" class="bg-white rounded-lg shadow-sm hover:shadow-lg transition group">
            <div class="relative">
              <img 
                :src="product.image" 
                :alt="product.name"
                class="w-full h-80 object-cover rounded-t-lg"
              >
              
              <!-- Discount Badge -->
              <div class="absolute top-4 left-4 bg-green-500 text-white px-3 py-1 rounded-full text-sm font-medium">
                {{ product.discount }}% off
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
              
              <!-- Countdown Timer (for first product) -->
              <div v-if="product.id === 1" class="absolute bottom-4 left-4 right-4 bg-white/90 backdrop-blur-sm rounded-lg p-3">
                <div class="flex justify-between text-sm">
                  <div class="text-center">
                    <div class="font-bold text-lg">{{ product.countdown.days }}</div>
                    <div class="text-gray-500">Days</div>
                  </div>
                  <div class="text-center">
                    <div class="font-bold text-lg">{{ product.countdown.hours }}</div>
                    <div class="text-gray-500">Hours</div>
                  </div>
                  <div class="text-center">
                    <div class="font-bold text-lg">{{ product.countdown.minutes }}</div>
                    <div class="text-gray-500">Mins</div>
                  </div>
                  <div class="text-center">
                    <div class="font-bold text-lg">{{ product.countdown.seconds }}</div>
                    <div class="text-gray-500">Sec</div>
                  </div>
                </div>
              </div>
            </div>
            
            <div class="p-6">
              <div class="text-sm text-gray-500 mb-2">{{ product.category }}</div>
              <h3 class="text-xl font-semibold text-gray-900 mb-2">{{ product.name }}</h3>
              
              <!-- Rating -->
              <div class="flex items-center space-x-1 mb-4">
                <div class="flex text-yellow-400">
                  <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 fill-current" viewBox="0 0 24 24">
                    <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                  </svg>
                </div>
                <span class="text-sm text-gray-600 ml-2">{{ product.rating }}</span>
              </div>
              
              <!-- Price -->
              <div class="flex items-center space-x-2 mb-4">
                <span class="text-2xl font-bold text-gray-900">${{ product.price.toFixed(2) }}</span>
                <span class="text-lg text-gray-500 line-through">${{ product.originalPrice.toFixed(2) }}</span>
              </div>
              
              <!-- Description -->
              <p class="text-gray-600 text-sm mb-4">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt
              </p>
              
              <!-- Shop Now Button -->
              <button class="w-full bg-primary text-white py-3 rounded-lg font-medium hover:bg-primary/90 transition flex items-center justify-center space-x-2">
                <span>Shop Now</span>
                <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                </svg>
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Limited Time Offers Section -->
    <LimitedTimeOffers />

    <!-- Promotional Banners Section -->
    <PromotionalBanners />

    <!-- Testimonials and Blog Section -->
    <TestimonialsAndBlog />

    <!-- FAQ Section -->
    <FAQ />

    <!-- Newsletter Section -->
    <Newsletter />
  </div>
</template>

