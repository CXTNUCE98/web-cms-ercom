<script setup lang="ts">
import { ref } from 'vue';

const activeFAQ = ref(1);

const faqs = [
  {
    id: 1,
    question: "How can I place an order?",
    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  },
  {
    id: 2,
    question: "What payment methods do you accept?",
    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  },
  {
    id: 3,
    question: "Can I track my order after it's been placed?",
    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  },
  {
    id: 4,
    question: "Do you offer customer support?",
    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  },
  {
    id: 5,
    question: "What is your return policy?",
    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  },
  {
    id: 6,
    question: "How to Create Account?",
    answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
  }
];

const toggleFAQ = (id: number) => {
  activeFAQ.value = activeFAQ.value === id ? 0 : id;
};
</script>

<template>
  <!-- FAQ Section -->
  <section class="py-16 bg-white">
    <div class="container mx-auto px-4">
      <div class="text-center mb-12">
        <p class="text-sm text-gray-500 mb-2">FAQ</p>
        <h2 class="text-4xl font-bold text-gray-900">Questions? Look here.</h2>
      </div>
      
      <div class="max-w-4xl mx-auto">
        <div class="space-y-4">
          <div 
            v-for="faq in faqs" 
            :key="faq.id"
            class="border border-gray-200 rounded-lg overflow-hidden"
          >
            <!-- Question Button -->
            <button 
              @click="toggleFAQ(faq.id)"
              class="w-full px-6 py-4 text-left bg-white hover:bg-gray-50 transition flex justify-between items-center"
            >
              <span class="font-medium text-gray-900">{{ faq.question }}</span>
              <svg 
                xmlns="http://www.w3.org/2000/svg" 
                class="h-5 w-5 text-gray-500 transition-transform"
                :class="{ 'rotate-45': activeFAQ === faq.id }"
                fill="none" 
                viewBox="0 0 24 24" 
                stroke="currentColor"
              >
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6v6m0 0v6m0-6h6m-6 0H6" />
              </svg>
            </button>
            
            <!-- Answer Content -->
            <div 
              v-if="activeFAQ === faq.id"
              class="px-6 py-4 bg-primary text-white"
            >
              <p class="text-sm leading-relaxed">{{ faq.answer }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

