<template>
  <section 
    :class="[
      'w-full max-w-[1500px] mx-auto px-4 sm:px-6 lg:px-8 font-sans space-y-6 transition-colors duration-200',
      isDarkMode ? 'dark' : ''
    ]"
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <!-- TOP ROW: APP DOWNLOAD BANNER + AI ASSISTANT BANNER -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-4 lg:gap-6">
      
      <!-- APP DOWNLOAD BANNER -->
      <div class="bg-[#faf7f2] dark:bg-stone-900/90 hover:bg-[#fffdfa] dark:hover:bg-stone-900 rounded-2xl p-4 sm:p-5 border-2 border-[#e6ded5] dark:border-stone-800 hover:border-[#702923] dark:hover:border-amber-500 shadow-md hover:shadow-xl transition-all duration-300 flex flex-col sm:flex-row items-center justify-between gap-4 relative overflow-hidden">
        
        <!-- Phone Mockups Image -->
        <div class="w-20 sm:w-24 md:w-28 shrink-0 z-10">
          <img 
            src="/urauth.png" 
            :alt="currentLang === 'ar' ? 'تطبيق أور' : 'Ur App'" 
            class="w-full h-auto object-contain drop-shadow-md"
          />
        </div>

        <!-- Text & Action Buttons -->
        <div class="flex-grow text-center z-10 space-y-2.5">
          <h3 class="text-lg sm:text-xl font-black text-[#702923] dark:text-amber-400">
            {{ currentLang === 'ar' ? 'حمل تطبيق بوابة أور' : 'Download Ur Portal App' }}
          </h3>
          <p class="text-xs sm:text-sm text-stone-600 dark:text-stone-300 font-bold">
            {{ currentLang === 'ar' ? 'وتواصل مع خدماتك الحكومية في أي وقت' : 'Access government services anytime, anywhere' }}
          </p>
          
          <!-- App Store Buttons -->
          <div class="flex flex-wrap items-center justify-center gap-2.5 pt-1">
            <!-- App Store Button -->
            <a 
              href="#" 
              class="bg-stone-900 hover:bg-stone-800 dark:bg-stone-800 dark:hover:bg-stone-700 text-white px-3.5 py-2 rounded-xl flex items-center gap-2 transition-colors shadow-sm shrink-0"
            >
              <Icon icon="mdi:apple" class="w-6 h-6 shrink-0" />
              <div :class="[currentLang === 'ar' ? 'text-right' : 'text-left', 'leading-tight']">
                <span class="block text-[9px] text-stone-300 uppercase tracking-wider">Download on the</span>
                <span class="block text-xs font-bold">App Store</span>
              </div>
            </a>
            
            <!-- Google Play Button -->
            <a 
              href="#" 
              class="bg-stone-900 hover:bg-stone-800 dark:bg-stone-800 dark:hover:bg-stone-700 text-white px-3.5 py-2 rounded-xl flex items-center gap-2 transition-colors shadow-sm shrink-0"
            >
              <Icon icon="mdi:google-play" class="w-6 h-6 shrink-0" />
              <div :class="[currentLang === 'ar' ? 'text-right' : 'text-left', 'leading-tight']">
                <span class="block text-[9px] text-stone-300 uppercase tracking-wider">GET IT ON</span>
                <span class="block text-xs font-bold">Google Play</span>
              </div>
            </a>
          </div>
        </div>

        <!-- View Details Link -->
        <a 
          href="#" 
          class="flex items-center gap-1 text-sm sm:text-base font-black text-stone-700 dark:text-stone-300 hover:text-[#702923] dark:hover:text-amber-400 shrink-0 z-10 transition-colors self-end sm:self-center"
        >
          <span>{{ currentLang === 'ar' ? 'التفاصيل' : 'Details' }}</span>
          <Icon 
            :icon="currentLang === 'ar' ? 'mdi:chevron-left' : 'mdi:chevron-right'" 
            class="w-4 h-4" 
          />
        </a>
      </div>

      <!-- AI ASSISTANT BANNER -->
      <div class="bg-[#faf7f2] dark:bg-stone-900/90 hover:bg-[#fffdfa] dark:hover:bg-stone-900 rounded-2xl p-4 sm:p-5 border-2 border-[#e6ded5] dark:border-stone-800 hover:border-[#702923] dark:hover:border-amber-500 shadow-md hover:shadow-xl transition-all duration-300 flex flex-col sm:flex-row items-center justify-between gap-4">
        
        <!-- Avatar Icon/Image -->
        <div class="w-16 h-16 sm:w-20 sm:h-20 rounded-2xl bg-[#702923]/10 dark:bg-amber-500/10 flex items-center justify-center shrink-0 overflow-hidden p-1">
          <img 
            src="/ai.png" 
            :alt="currentLang === 'ar' ? 'مساعد أور الذكي' : 'Ur AI Assistant'" 
            class="w-full h-full object-contain"
          />
        </div>

        <!-- Text & Input Area -->
        <div class="flex-grow w-full space-y-2">
          <h3 class="text-base sm:text-lg font-black text-[#702923] dark:text-amber-400 text-center sm:text-start">
            {{ currentLang === 'ar' ? 'مرحباً، أنا مساعد أور الذكي' : 'Hello, I am Ur AI Assistant' }}
          </h3>
          <p class="text-xs sm:text-sm text-stone-600 dark:text-stone-300 font-bold text-center sm:text-start">
            {{ currentLang === 'ar' ? 'يمكنني مساعدتك في العثور على الخدمة المناسبة' : 'I can help you find the right government service' }}
          </p>

          <div class="relative flex items-center mt-2 w-full">
            <input 
              type="text" 
              :placeholder="currentLang === 'ar' ? 'اكتب سؤالك هنا...' : 'Type your question here...'" 
              class="w-full bg-stone-100/90 dark:bg-stone-800 border-2 border-stone-200/80 dark:border-stone-700 rounded-full py-2.5 px-4 text-xs sm:text-sm font-semibold text-stone-800 dark:text-stone-100 focus:outline-none focus:bg-white dark:focus:bg-stone-900 focus:border-[#702923] dark:focus:border-amber-500 shadow-inner transition-all"
              :class="currentLang === 'ar' ? 'pl-12 pr-4' : 'pr-12 pl-4'"
            />
            <button 
              class="absolute w-8 h-8 rounded-full bg-[#702923] dark:bg-amber-600 text-white flex items-center justify-center hover:bg-[#521d18] dark:hover:bg-amber-700 transition-colors shadow-sm"
              :class="currentLang === 'ar' ? 'left-1.5' : 'right-1.5'"
              :aria-label="currentLang === 'ar' ? 'إرسال' : 'Send'"
            >
              <Icon 
                :icon="currentLang === 'ar' ? 'mdi:send' : 'mdi:send-outline'" 
                class="w-4 h-4 transform"
                :class="currentLang === 'ar' ? 'rotate-180' : ''"
              />
            </button>
          </div>
        </div>
      </div>

    </div>

    <!-- BOTTOM STATS BAR -->
    <div class="bg-white/60 dark:bg-stone-900/80 backdrop-blur-md rounded-2xl p-4 border border-stone-200/70 dark:border-stone-800 shadow-sm grid grid-cols-2 md:grid-cols-4 gap-4 divide-y md:divide-y-0 md:divide-x md:divide-x-reverse dark:divide-stone-800 divide-stone-200 transition-colors">
      
      <!-- Stat 1 -->
      <div class="flex items-center justify-center gap-3 p-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 dark:bg-amber-500/10 text-[#702923] dark:text-amber-400 flex items-center justify-center shrink-0">
          <Icon icon="mdi:office-building" class="w-5 h-5" />
        </div>
        <div :class="currentLang === 'ar' ? 'text-right' : 'text-left'">
          <p class="font-extrabold text-stone-900 dark:text-stone-100 text-sm">1,200+</p>
          <p class="text-[11px] text-stone-500 dark:text-stone-400 font-medium">
            {{ currentLang === 'ar' ? 'جهة حكومية مرتبطة' : 'Linked Govt Entities' }}
          </p>
        </div>
      </div>

      <!-- Stat 2 -->
      <div class="flex items-center justify-center gap-3 p-2 pt-4 md:pt-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 dark:bg-amber-500/10 text-[#702923] dark:text-amber-400 flex items-center justify-center shrink-0">
          <Icon icon="mdi:file-document-outline" class="w-5 h-5" />
        </div>
        <div :class="currentLang === 'ar' ? 'text-right' : 'text-left'">
          <p class="font-extrabold text-stone-900 dark:text-stone-100 text-sm">2,000+</p>
          <p class="text-[11px] text-stone-500 dark:text-stone-400 font-medium">
            {{ currentLang === 'ar' ? 'خدمة إلكترونية' : 'E-Services Available' }}
          </p>
        </div>
      </div>

      <!-- Stat 3 -->
      <div class="flex items-center justify-center gap-3 p-2 pt-4 md:pt-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 dark:bg-amber-500/10 text-[#702923] dark:text-amber-400 flex items-center justify-center shrink-0">
          <Icon icon="mdi:account-group" class="w-5 h-5" />
        </div>
        <div :class="currentLang === 'ar' ? 'text-right' : 'text-left'">
          <p class="font-extrabold text-stone-900 dark:text-stone-100 text-sm">+10,000,000</p>
          <p class="text-[11px] text-stone-500 dark:text-stone-400 font-medium">
            {{ currentLang === 'ar' ? 'مستخدم مسجل' : 'Registered Users' }}
          </p>
        </div>
      </div>

      <!-- Stat 4 -->
      <div class="flex items-center justify-center gap-3 p-2 pt-4 md:pt-2">
        <div class="w-10 h-10 rounded-full bg-[#702923]/10 dark:bg-amber-500/10 text-[#702923] dark:text-amber-400 flex items-center justify-center shrink-0">
          <Icon icon="mdi:clock-fast" class="w-5 h-5" />
        </div>
        <div :class="currentLang === 'ar' ? 'text-right' : 'text-left'">
          <p class="font-extrabold text-stone-900 dark:text-stone-100 text-sm">24/7</p>
          <p class="text-[11px] text-stone-500 dark:text-stone-400 font-medium">
            {{ currentLang === 'ar' ? 'خدمة على مدار الساعة' : '24/7 Service Support' }}
          </p>
        </div>
      </div>

    </div>

  </section>
</template>

<script>
import { Icon } from '@iconify/vue2';

export default {
  name: 'PromoBanners',
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