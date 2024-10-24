<script setup>
</script>

<template>
    <section class="relative bg-center h-screen w-full" style="background-image: url(/src/assets/Image Wrapper.png);">
  <div class="bg-cover bg-center h-screen" :style="bgImage">
    <!-- Navigation Bar -->
    <div class="flex flex-row justify-center bg-slate-800 text-orange-200 p-3 items-center w-1/3 mx-auto rounded-sm border-orange-400 border-solid border w-[650px] h-[75px]">
      <h2 class="text-[#DAC5A7] text-3xl -mt-1">robby.</h2>
      <h2 class="mr-7 ml-6">SERVICES</h2>
      <h2 class="mr-7">WORK</h2>
      <h2 class="mr-7">ABOUT</h2>
      <h2 class="mr-7">BLOG</h2>
      <h2 class="mr-7">PAGES</h2>
      <button class="bg-orange-100 text-black p-2 font-satoshi rounded-sm">LET'S TALK</button>
    </div>
  </div>

  <div class="flex justify-center mt-4">
  <img src="/src/assets/Grid.png" alt="Second Image" class="w-[650px] h-auto rounded-sm">
</div>
</section>
</template>

<script>
export default {
  data() {
    return {
      bgImage: {
        backgroundImage: "url('/src/assets/Image Wrapper.png')" // Replace with your image path
      }
    };
  }
};
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>

  