<template>
  <div 
    :class="[
      'home-page font-sans min-h-screen transition-colors duration-200',
      isDarkMode ? 'dark bg-stone-950 text-stone-100' : 'bg-[#faf7f2] text-stone-900'
    ]"
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <!-- HERO SECTION -->
    <HeroSec 
      :is-dark-mode="isDarkMode" 
      :current-lang="currentLang" 
    />

    <!-- UNIFIED BACKGROUND WRAPPER WITH DARK MODE SUPPORT -->
    <div 
      :class="[
        'bg-no-repeat bg-top bg-[length:100%_100%] py-8 sm:py-12 space-y-8 sm:space-y-12 transition-colors duration-200',
        isDarkMode ? 'bg-stone-950/90' : 'bg-[#f5f0ea]'
      ]"
      :style="!isDarkMode ? { backgroundImage: 'url(\'/bg2.png\')' } : {}"
    >
      <!-- SERVICES DIRECTORY -->
      <Services 
        :is-dark-mode="isDarkMode" 
        :current-lang="currentLang" 
      />

      <!-- LATEST NEWS SECTION -->
      <News 
        :is-dark-mode="isDarkMode" 
        :current-lang="currentLang" 
      />

      <!-- PROMO BANNERS / ANNOUNCEMENTS -->
      <PromoBanners 
        :is-dark-mode="isDarkMode" 
        :current-lang="currentLang" 
      />
    </div>
  </div>
</template>

<script>
import HeroSec from '@/components/homepage/HeroSec.vue'
import Services from '@/components/homepage/Services.vue'
import News from '@/components/homepage/News.vue'
import PromoBanners from '@/components/homepage/PromoBanners.vue'

export default {
  name: 'HomeView',
  components: {
    HeroSec,
    Services,
    News,
    PromoBanners
  },
  props: {
    isDarkMode: {
      type: Boolean,
      default: false
    },
    currentLang: {
      type: String,
      default: 'ar'
    }
  }
}
</script>