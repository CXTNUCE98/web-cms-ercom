<script setup lang="ts">
import { ref } from 'vue';

const activeTestimonial = ref(0);

const testimonials = [
  {
    name: "Leslie Alexander",
    role: "Fashion Enthusiast",
    rating: 5.0,
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
    image: "https://images.unsplash.com/photo-1494790108755-2616b612b786?w=100&h=100&fit=crop&crop=face"
  }
];

const blogPosts = [
  {
    title: "10 Fashion Trends for the Modern Woman",
    date: "22 March 2024",
    image: "https://images.unsplash.com/photo-1496747611176-843222e1e57c?w=400&h=250&fit=crop"
  },
  {
    title: "Fashion Forward: Tips, Trends, and Inspiration",
    date: "21 March 2024",
    image: "https://images.unsplash.com/photo-1515372039744-b8f02a3ae446?w=400&h=250&fit=crop"
  },
  {
    title: "Fall Fashion Frenzy: The Ultimate Style Guide",
    date: "20 March 2024",
    image: "https://images.unsplash.com/photo-1591047139829-d91aecb6caea?w=400&h=250&fit=crop"
  }
];
</script>

<template>
  <!-- Testimonials Section -->
  <section class="py-16 bg-gray-50">
    <div class="container mx-auto px-4">
      <div class="flex justify-between items-center mb-12">
        <h2 class="text-4xl font-bold text-gray-900">What Our Clients Say</h2>
        
        <!-- Navigation Arrows -->
        <div class="flex space-x-2">
          <button class="w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center hover:bg-orange-200 transition">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-orange-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
            </svg>
          </button>
          <button class="w-12 h-12 bg-primary rounded-full flex items-center justify-center hover:bg-primary/90 transition">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </button>
        </div>
      </div>
      
      <!-- Testimonial Card -->
      <div class="bg-gray-100 rounded-2xl p-8 lg:p-12">
        <div class="flex flex-col lg:flex-row items-center gap-8">
          <!-- Client Image -->
          <div class="flex-shrink-0">
            <img 
              :src="testimonials[0].image" 
              :alt="testimonials[0].name"
              class="w-32 h-32 rounded-full object-cover"
            >
          </div>
          
          <!-- Testimonial Content -->
          <div class="flex-1 text-center lg:text-left">
            <!-- Quote Icon -->
            <div class="text-6xl text-primary mb-4">"</div>
            
            <!-- Rating -->
            <div class="flex justify-center lg:justify-start items-center space-x-1 mb-4">
              <div class="flex text-yellow-400">
                <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 fill-current" viewBox="0 0 24 24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
              </div>
              <span class="text-lg font-semibold text-gray-700 ml-2">{{ testimonials[0].rating }}</span>
            </div>
            
            <!-- Quote Text -->
            <p class="text-lg text-gray-700 mb-6 leading-relaxed">
              {{ testimonials[0].content }}
            </p>
            
            <!-- Client Info -->
            <div>
              <h4 class="text-xl font-bold text-gray-900">{{ testimonials[0].name }}</h4>
              <p class="text-gray-600">{{ testimonials[0].role }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- News & Blog Section -->
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <p class="text-sm text-gray-500 mb-2">News & Blog</p>
        <h2 class="text-4xl font-bold text-gray-900">Our Latest News & Blogs</h2>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <article v-for="post in blogPosts" :key="post.title" class="bg-white rounded-lg shadow-sm hover:shadow-lg transition group">
          <div class="relative">
            <img 
              :src="post.image" 
              :alt="post.title"
              class="w-full h-48 object-cover rounded-t-lg group-hover:scale-105 transition-transform duration-300"
            >
            <!-- Date Overlay -->
            <div class="absolute bottom-4 right-4 bg-orange-500 text-white px-3 py-1 rounded-lg text-sm font-medium">
              {{ post.date }}
            </div>
          </div>
          
          <div class="p-6">
            <h3 class="text-xl font-bold text-gray-900 mb-4 group-hover:text-primary transition">
              {{ post.title }}
            </h3>
            <p class="text-gray-600 text-sm mb-4">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
            </p>
            <a href="#" class="text-primary font-medium hover:underline">
              Read More
            </a>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

