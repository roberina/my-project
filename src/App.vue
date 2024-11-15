<template>
  <div class="bg-black">
    <HelloWorld></HelloWorld>
  </div>

</template>

<script setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue';


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

<style>
@font-face {
  font-family: 'ArcadeClassic';
  src: url('https://db.onlinewebfonts.com/t/a1f56a3a324d41d6b503bda6e51c0e82.woff2') format('woff2');
  font-weight: normal;
  font-style: normal;
}

.font-arcade {
  font-family: 'ArcadeClassic', monospace;
  letter-spacing: 0.1em;
}

</style>