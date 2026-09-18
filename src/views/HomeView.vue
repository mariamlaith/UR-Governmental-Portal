<template>
  <div class="home-page font-sans">
    <!-- Hero Section -->
    <HeroSec />

    <!-- UNIFIED BACKGROUND WRAPPER WITH BASE FALLBACK COLOR -->
    <div 
      class="bg-[#f5f0ea] bg-no-repeat bg-top bg-[length:100%_100%] py-10 space-y-10"
      style="background-image: url('/bg2.png');"
    >
      <Services />
      <News />
      <PromoBanners />
    </div>
  </div>
</template>

<script setup>
import HeroSec from '@/components/homepage/HeroSec.vue'
import Services from '@/components/homepage/Services.vue'
import News from '@/components/homepage/News.vue'
import PromoBanners from '@/components/homepage/PromoBanners.vue'
</script>