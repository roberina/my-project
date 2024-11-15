<template>
   <div class="min-h-screen bg-black">
    
    <nav class="p-4 border-b text-[#f5d536]">
      <div class="container mx-auto flex items-center justify-between">
        
        <router-link to="/" class="relative group">
          <h1 class="font-arcade text-3xl text-transparent bg-gradient-to-b from-yellow-400 to-yellow-600 bg-clip-text relative z-10">
            ROBBY
          </h1>
          <h1 class="font-arcade text-3xl text-[#f5d536] absolute top-0 left-0 blur-sm z-0 group-hover:blur-md transition-all">
            ROBBY
          </h1>
        </router-link>

        
        <div class="hidden md:flex items-center space-x-8">
          <router-link 
            v-for="item in mainNavItems" 
            :key="item.path" 
            :to="item.path"
            class="text-[#f5d536] hover:text-yellow-400 transition-colors text-sm tracking-wider"
          >
            {{ item.name }}
          </router-link>
          
          
          <div class="relative group">
            <button 
              class="text--500 hover:text-green-400 transition-colors flex items-center text-sm tracking-wider"
              @click="togglePages"
            >
              PAGES
              <svg 
                class="w-4 h-4 ml-1" 
                fill="none" 
                stroke="currentColor" 
                viewBox="0 0 24 24"
              >
                <path d="M19 9l-7 7-7-7" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </button>
            
            
            <div 
              v-if="showPages"
              class="absolute left-0 mt-2 w-48 bg-black border text-[#f5d536] shadow-lg py-2"
            >
              <router-link 
                v-for="page in pageItems" 
                :key="page.path" 
                :to="page.path"
                class="block px-4 py-2 text-[#f5d536] hover:text-yellow-400 transition-colors text-sm"
              >
                {{ page.name }}
              </router-link>
            </div>
          </div>
        </div>

        
        <router-link 
          to="/contact"
          class="bg-yellow-500 text-black px-6 py-2 text-sm tracking-wider hover:bg-yellow-400 transition-colors relative group"
        >
          LET'S TALK
          <div class="absolute inset-0 bg-yellow-500 blur-sm -z-10 group-hover:blur-md transition-all"></div>
        </router-link>

        
        <button 
          class="md:hidden text-[#f5d536] hover:text-yellow-400 transition-colors"
          @click="toggleMobileMenu"
        >
          <svg 
            class="w-6 h-6" 
            fill="none" 
            stroke="currentColor" 
            viewBox="0 0 24 24"
          >
            <path 
              v-if="!showMobileMenu"
              d="M4 6h16M4 12h16M4 18h16" 
              stroke-width="2" 
              stroke-linecap="round"
            />
            <path 
              v-else
              d="M6 18L18 6M6 6l12 12" 
              stroke-width="2" 
              stroke-linecap="round"
            />
          </svg>
        </button>
      </div>

      
      <div 
        v-if="showMobileMenu"
        class="md:hidden mt-4 space-y-4 border-t text-[#f5d536] pt-4"
      >
        <router-link 
          v-for="item in mainNavItems" 
          :key="item.path" 
          :to="item.path"
          class="block text-[#f5d536] hover:text-yellow-400 transition-colors text-sm tracking-wider"
        >
          {{ item.name }}
        </router-link>
        <div class="space-y-2">
          <div 
            class="text-[#f5d536] cursor-pointer text-sm tracking-wider"
            @click="toggleMobilePages"
          >
            PAGES
          </div>
          <div 
            v-if="showMobilePages"
            class="pl-4 space-y-2"
          >
            <router-link 
              v-for="page in pageItems" 
              :key="page.path" 
              :to="page.path"
              class="block text-[#f5d536] hover:text-yellow-400 transition-colors text-sm"
            >
              {{ page.name }}
            </router-link>
          </div>
        </div>
      </div>
    </nav>

    
    <div class="flex items-center justify-center  h-[calc(100vh-5rem)]">
      <h2 class="font-arcade text-[4vw] text-[#f5d536]">
        WEB DESIGNER AND DEVELOPER
      </h2>
    </div>
  </div>
  <div class="min-h-screen bg-black">

    
    <div class="container mx-auto px-4 py-20">
      <h2 class="font-arcade text-4xl text-[#f5d536] text-center mb-16">
        Your Website
        <span class="block text-2xl mt-2 opacity-80">in 5 steps</span>
      </h2>

      
      <div class="relative">
        
        <div class="absolute left-8 top-0 bottom-0 w-px bg-green-500/20 md:left-1/2"></div>

        
        <div class="space-y-24">
         
          <div class="relative flex flex-col md:flex-row items-start group">
            <div class="flex-1 md:text-right md:pr-12">
              <div class="bg-black/50 border text-[#f5d536] p-6 rounded-lg backdrop-blur-sm
                         transform transition-all duration-300 hover:border-yellow-500/40 hover:scale-105">
                <h3 class="font-arcade text-[#f5d536] text-xl mb-4">01. DISCOVERY CALL</h3>
                <p class="text-yellow-400/70">Let's get aligned on your goals. We'll discuss your vision, requirements, and timeline to ensure we create the perfect digital presence for your business.</p>
                <ul class="mt-4 text-yellow-400/60 space-y-2">
                  <li>• Digital & Brand Audit</li>
                  <li>• Goals & Timeline Planning</li>
                  <li>• Project Scope Definition</li>
                </ul>
              </div>
            </div>
            <div class="absolute left-8 w-4 h-4 rounded-full bg-yellow-500 md:left-1/2 md:-ml-2 mt-2">
              <div class="absolute w-full h-full rounded-full bg-yellow-500 animate-ping opacity-25"></div>
            </div>
            <div class="flex-1 md:pl-12"></div>
          </div>

          
          <div class="relative flex flex-col md:flex-row items-start group">
            <div class="flex-1 md:text-right md:pr-12"></div>
            <div class="absolute left-8 w-4 h-4 rounded-full bg-yellow-500 md:left-1/2 md:-ml-2 mt-2">
              <div class="absolute w-full h-full rounded-full bg-yellow-500 animate-ping opacity-25"></div>
            </div>
            <div class="flex-1 md:pl-12">
              <div class="bg-black/50 border border-yellow-500/20 p-6 rounded-lg backdrop-blur-sm
                         transform transition-all duration-300 hover:border-yellow-500/40 hover:scale-105">
                <h3 class="font-arcade text-[#f5d536] text-xl mb-4">02. CONCEPT & STRATEGY</h3>
                <p class="text-yellow-400/70">Together, we'll develop a strategy that resonates with your target audience while meeting all technical requirements.</p>
                <ul class="mt-4 text-yellow-400/60 space-y-2">
                  <li>• UX Strategy</li>
                  <li>• Wireframing</li>
                  <li>• Content Strategy</li>
                </ul>
              </div>
            </div>
          </div>

          
          <div class="relative flex flex-col md:flex-row items-start group">
            <div class="flex-1 md:text-right md:pr-12">
              <div class="bg-black/50 border border-yellow-500/20 p-6 rounded-lg backdrop-blur-sm
                         transform transition-all duration-300 hover:border-yellow-500/40 hover:scale-105">
                <h3 class="font-arcade text-[#f5d536] text-xl mb-4">03. WEB DESIGN</h3>
                <p class="text-yellow-400/70">We'll create a custom design that captures your brand's essence while ensuring an intuitive user experience.</p>
                <ul class="mt-4 text-yellow-400/60 space-y-2">
                  <li>• High-end Design Creation</li>
                  <li>• Responsive Layouts</li>
                  <li>• Interactive Elements</li>
                </ul>
              </div>
            </div>
            <div class="absolute left-8 w-4 h-4 rounded-full bg-yellow-500 md:left-1/2 md:-ml-2 mt-2">
              <div class="absolute w-full h-full rounded-full bg-yellow-500 animate-ping opacity-25"></div>
            </div>
            <div class="flex-1 md:pl-12"></div>
          </div>

          
          <div class="relative flex flex-col md:flex-row items-start group">
            <div class="flex-1 md:text-right md:pr-12"></div>
            <div class="absolute left-8 w-4 h-4 rounded-full bg-yellow-500 md:left-1/2 md:-ml-2 mt-2">
              <div class="absolute w-full h-full rounded-full bg-yellow-500 animate-ping opacity-25"></div>
            </div>
            <div class="flex-1 md:pl-12">
              <div class="bg-black/50 border text-[#f5d536] p-6 rounded-lg backdrop-blur-sm
                         transform transition-all duration-300 hover:border-yellow-500/40 hover:scale-105">
                <h3 class="font-arcade text-[#f5d536] text-xl mb-4">04. DEVELOPMENT</h3>
                <p class="text-[#f5d536]">Bringing the design to life with clean, efficient code and modern development practices.</p>
                <ul class="mt-4 text-[#f5d536] space-y-2">
                  <li>• Modern Tech Stack</li>
                  <li>• Mobile-first Strategy</li>
                  <li>• SEO Integration</li>
                </ul>
              </div>
            </div>
          </div>

         
          <div class="relative flex flex-col md:flex-row items-start group">
            <div class="flex-1 md:text-right md:pr-12">
              <div class="bg-black/50 border text-[#f5d536] p-6 rounded-lg backdrop-blur-sm
                         transform transition-all duration-300 hover:border-green-500/40 hover:scale-105">
                <h3 class="font-arcade text-[#f5d536] text-xl mb-4">05. WEBSITE OPTIMIZATION</h3>
                <p class="text-[#f5d536]">Final testing, optimization, and launch preparation to ensure everything runs smoothly.</p>
                <ul class="mt-4 text-[#f5d536] space-y-2">
                  <li>• Performance Testing</li>
                  <li>• Analytics Setup</li>
                  <li>• Launch & Support</li>
                </ul>
              </div>
            </div>
            <div class="absolute left-8 w-4 h-4 rounded-full bg-yellow-500 md:left-1/2 md:-ml-2 mt-2">
              <div class="absolute w-full h-full rounded-full bg-yellow-500 animate-ping opacity-25"></div>
            </div>
            <div class="flex-1 md:pl-12"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="min-h-screen bg-black">
  <div class="container mx-auto px-4 py-20">
    <h2 class="font-arcade text-4xl text-[#f5d536] text-center mb-16">
      Reviews from My Clients
      <span class="block text-2xl mt-2 opacity-80">What They Say</span>
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
      <!-- Example Review Card -->
      <div 
        v-for="(review, index) in reviews" 
        :key="index" 
        class="bg-black/50 border text-[#f5d536] p-6 rounded-lg backdrop-blur-sm
               transform transition-all duration-300 hover:border-yellow-500/40 hover:scale-105"
      >
        <h3 class="text-[#f5d536] text-xl font-arcade mb-4">{{ review.name }}</h3>
        <p class="text-[#f5d536] mb-4">{{ review.text }}</p>
        <div class="text-[#f5d536]">
          <span v-for="n in review.rating" :key="n">★</span>
          <span v-for="n in (5 - review.rating)" :key="n">☆</span>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script setup>
import { ref } from 'vue'


const mainNavItems = [
  { name: 'SERVICES', path: '/services' },
  { name: 'WORK', path: '/work' },
  { name: 'ABOUT', path: '/about' },
  { name: 'BLOG', path: '/blog' },
]

const pageItems = [
  { name: 'Team', path: '/team' },
  { name: 'Pricing', path: '/pricing' },
  { name: 'FAQ', path: '/faq' },
  { name: 'Contact', path: '/contact' },
]

// State management
const showPages = ref(false)
const showMobileMenu = ref(false)
const showMobilePages = ref(false)

// Toggle functions
const togglePages = () => {
  showPages.value = !showPages.value
}

const toggleMobileMenu = () => {
  showMobileMenu.value = !showMobileMenu.value
  if (!showMobileMenu.value) {
    showMobilePages.value = false 
  }
}

const toggleMobilePages = () => {
  showMobilePages.value = !showMobilePages.value
}

const reviews = [
  { name: 'Kennu1453', text: 'Amazing work! Truly exceeded expectations.', rating: 5 },
  { name: 'Ken', text: 'Professional and timely. Highly recommend!', rating: 4 },
  { name: 'Martti', text: 'Great experience from start to finish.', rating: 5 },
]

</script>