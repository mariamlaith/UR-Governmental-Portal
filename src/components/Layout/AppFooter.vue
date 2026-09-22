<template>
  <footer 
    :class="[
      'w-full font-sans transition-colors duration-200 border-t',
      isDarkMode 
        ? 'bg-stone-950 text-stone-300 border-stone-800' 
        : 'bg-[#1e110c] text-stone-200 border-stone-900'
    ]"
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <div class="pt-12 pb-8">
      
      <!-- MAIN GRID CONTAINER -->
      <div class="max-w-[1500px] mx-auto px-4 sm:px-8 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 lg:gap-14 pb-10 border-b border-stone-800">
        
        <!-- Column 1: Logo & Social Links -->
        <div class="flex flex-col items-start gap-5">
          <a href="#" class="inline-block shrink-0">
            <img 
              src="/urlogotrans.png" 
              alt="بوابة أور" 
              class="h-20 sm:h-24 md:h-28 w-auto object-contain transition-all" 
            />
          </a>
          
          <p class="text-xs sm:text-sm text-stone-400 max-w-xs leading-relaxed">
            {{ currentLang === 'ar' 
              ? 'البوابة الإلكترونية الوطنية للخدمات الحكومية في جمهورية العراق.' 
              : 'The national electronic portal for government services in the Republic of Iraq.' 
            }}
          </p>

          <!-- Social Icons (Powered by Iconify) -->
          <div class="flex items-center gap-2.5 mt-1 flex-wrap">
            <a 
              href="#" 
              class="w-10 h-10 rounded-full bg-stone-800/80 hover:bg-[#702923] dark:hover:bg-amber-600 flex items-center justify-center text-stone-200 transition-colors" 
              title="Facebook"
            >
              <Icon icon="mdi:facebook" class="w-5 h-5" />
            </a>
            <a 
              href="#" 
              class="w-10 h-10 rounded-full bg-stone-800/80 hover:bg-[#702923] dark:hover:bg-amber-600 flex items-center justify-center text-stone-200 transition-colors" 
              title="LinkedIn"
            >
              <Icon icon="mdi:linkedin" class="w-5 h-5" />
            </a>
            <a 
              href="#" 
              class="w-10 h-10 rounded-full bg-stone-800/80 hover:bg-[#702923] dark:hover:bg-amber-600 flex items-center justify-center text-stone-200 transition-colors" 
              title="Instagram"
            >
              <Icon icon="mdi:instagram" class="w-5 h-5" />
            </a>
            <a 
              href="#" 
              class="w-10 h-10 rounded-full bg-stone-800/80 hover:bg-[#702923] dark:hover:bg-amber-600 flex items-center justify-center text-stone-200 transition-colors" 
              title="X"
            >
              <Icon icon="ri:twitter-x-fill" class="w-4 h-4" />
            </a>
            <a 
              href="#" 
              class="w-10 h-10 rounded-full bg-stone-800/80 hover:bg-[#702923] dark:hover:bg-amber-600 flex items-center justify-center text-stone-200 transition-colors" 
              title="TikTok"
            >
              <Icon icon="ic:baseline-tiktok" class="w-5 h-5" />
            </a>
            <a 
              href="#" 
              class="w-10 h-10 rounded-full bg-stone-800/80 hover:bg-[#702923] dark:hover:bg-amber-600 flex items-center justify-center text-stone-200 transition-colors" 
              title="YouTube"
            >
              <Icon icon="mdi:youtube" class="w-5 h-5" />
            </a>
          </div>
        </div>

        <!-- Column 2: Legal Links -->
        <div class="space-y-4 text-base">
          <p class="font-bold text-white text-lg pb-2 border-b border-stone-800/80">
            {{ currentLang === 'ar' ? 'عن المنصة' : 'About Platform' }}
          </p>
          <ul class="space-y-2.5 text-stone-300 dark:text-stone-400 font-medium text-sm sm:text-base">
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'عن أور' : 'About Ur' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'سياسة الخصوصية' : 'Privacy Policy' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'شروط الاستخدام' : 'Terms of Use' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'اتصل بنا' : 'Contact Us' }}</a></li>
          </ul>
        </div>

        <!-- Column 3: Quick Navigation -->
        <div class="space-y-4 text-base">
          <p class="font-bold text-white text-lg pb-2 border-b border-stone-800/80">
            {{ currentLang === 'ar' ? 'روابط سريعة' : 'Quick Links' }}
          </p>
          <ul class="space-y-2.5 text-stone-300 dark:text-stone-400 font-medium text-sm sm:text-base">
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'الخدمات الإلكترونية' : 'E-Services' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'الخدمات المقترحة' : 'Suggested Services' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'المستندات الإلكترونية' : 'E-Documents' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'الجهات الخدمية' : 'Service Entities' }}</a></li>
            <li><a href="#" class="hover:text-amber-400 transition-colors">{{ currentLang === 'ar' ? 'المواقع الحكومية' : 'Government Sites' }}</a></li>
          </ul>
        </div>

      </div>

      <!-- COPYRIGHT BOTTOM LINE -->
      <div class="max-w-[1500px] mx-auto px-4 sm:px-8 pt-6 flex flex-col sm:flex-row justify-between items-center text-xs sm:text-sm text-stone-400 gap-2 font-medium">
        <p>
          {{ currentLang === 'ar' 
            ? '© 2026 بوابة أور - جميع الحقوق محفوظة' 
            : '© 2026 Ur Portal - All Rights Reserved' 
          }}
        </p>
        <p>
          {{ currentLang === 'ar' 
            ? 'منصة الخدمات الحكومية الإلكترونية' 
            : 'Electronic Government Services Platform' 
          }}
        </p>
      </div>

    </div>
  </footer>
</template>

<script>
import { Icon } from '@iconify/vue2';

export default {
  name: 'AppFooter',
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