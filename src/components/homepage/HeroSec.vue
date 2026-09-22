<template>
  <section 
    :class="[
      'relative w-full min-h-[420px] sm:min-h-[480px] md:h-[520px] bg-cover bg-center font-sans overflow-hidden flex items-end transition-colors duration-200',
      isDarkMode ? 'dark' : ''
    ]"
    style="background-image: url('/urbg.png');" 
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <!-- Keep the source image bright in light mode; add contrast only for dark mode. -->
    <div class="absolute inset-0 bg-transparent dark:bg-black/60 transition-colors"></div>

    <!-- MAIN CONTAINER -->
    <div class="relative w-full max-w-[1500px] mx-auto px-4 sm:px-8 pb-8 sm:pb-12 md:pb-16 flex flex-col items-center">
          

      <!-- SEARCH BAR CONTAINER -->
      <div class="w-full max-w-3xl">
        <div class="bg-white/95 dark:bg-stone-900/95 backdrop-blur-md rounded-2xl sm:rounded-full shadow-2xl p-2 flex flex-col sm:flex-row items-center gap-2 border border-stone-200/80 dark:border-stone-800 transition-colors">
          
          <!-- Input Text Area -->
          <div class="w-full flex items-center gap-2 px-3 py-1">
            <Icon icon="mdi:magnify" class="w-5 h-5 text-stone-400 shrink-0" />
            <input 
              type="text" 
              :placeholder="currentLang === 'ar' ? 'ابحث عن خدمة، معاملة، أو جهة حكومية...' : 'Search for a service, transaction, or government entity...'" 
              class="w-full bg-transparent text-stone-800 dark:text-stone-100 text-sm md:text-base focus:outline-none placeholder-stone-400 dark:placeholder-stone-500 font-medium"
            />
          </div>

          <!-- Categories Dropdown Button (Desk/Tablet view) -->
          <div 
            :class="[
              'hidden sm:flex items-center gap-2 pr-4 pl-3 text-stone-700 dark:text-stone-300 hover:text-stone-900 dark:hover:text-white cursor-pointer shrink-0 transition-colors',
              currentLang === 'ar' ? 'border-r border-stone-300 dark:border-stone-700' : 'border-l border-stone-300 dark:border-stone-700'
            ]"
          >
            <Icon icon="mdi:format-list-bulleted" class="w-5 h-5 text-[#702923] dark:text-amber-500" />
            <span class="text-xs md:text-sm font-bold whitespace-nowrap">
              {{ currentLang === 'ar' ? 'تصفح حسب الوزارات' : 'Browse by Ministry' }}
            </span>
            <Icon icon="mdi:chevron-down" class="w-4 h-4 text-stone-500" />
          </div>

          <!-- Search Button -->
          <button 
            class="w-full sm:w-auto bg-[#702923] hover:bg-[#521d18] dark:bg-amber-600 dark:hover:bg-amber-700 text-white px-6 py-3 rounded-xl sm:rounded-full font-bold text-sm transition-colors flex items-center justify-center gap-2 shrink-0 shadow-md"
          >
            <Icon icon="mdi:magnify" class="w-5 h-5 sm:hidden" />
            <span>{{ currentLang === 'ar' ? 'بحث' : 'Search' }}</span>
          </button>

        </div>
      </div>

    </div>
  </section>
</template>

<script>
import { Icon } from '@iconify/vue2';

export default {
  name: 'HeroSection',
  components: {
    Icon
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
};
</script>