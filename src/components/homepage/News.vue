<template>
  <section 
    :class="[
      'w-full px-4 sm:px-6 lg:px-8 py-6 font-sans transition-colors duration-200',
      isDarkMode ? 'dark' : ''
    ]" 
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <div class="max-w-[1500px] mx-auto">
      
      <!-- HEADER ROW -->
      <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 pb-4 mb-6 border-b border-[#e2d7c7]/80 dark:border-stone-800">
        <!-- Title & Subtitle -->
        <div class="flex items-center gap-3.5">
          <div class="p-3 bg-[#702923]/10 dark:bg-amber-500/10 text-[#702923] dark:text-amber-500 rounded-xl shrink-0">
            <Icon icon="mdi:newspaper-variant-outline" class="w-7 h-7" />
          </div>
          <div>
            <h2 class="text-xl sm:text-2xl font-black text-stone-900 dark:text-stone-100">
              {{ currentLang === 'ar' ? 'آخر الأخبار' : 'Latest News' }}
            </h2>
            <p class="text-xs sm:text-sm text-stone-600 dark:text-stone-400 font-bold mt-0.5">
              {{ currentLang === 'ar' ? 'أحدث الأخبار والقرارات الحكومية' : 'Latest government updates and announcements' }}
            </p>
          </div>
        </div>

        <!-- View All Link -->
        <a 
          href="#" 
          class="flex items-center gap-1.5 text-base font-extrabold text-[#702923] dark:text-amber-500 hover:text-[#521d18] dark:hover:text-amber-400 transition-colors self-end sm:self-auto"
        >
          <span>{{ currentLang === 'ar' ? 'اعرض جميع الأخبار' : 'View All News' }}</span>
          <Icon 
            :icon="currentLang === 'ar' ? 'mdi:arrow-left' : 'mdi:arrow-right'" 
            class="w-5 h-5" 
          />
        </a>
      </div>

      <!-- 4-CARD NEWS GRID -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
        <div 
          v-for="(item, index) in localizedNews" 
          :key="index"
          class="group bg-[#faf7f2] dark:bg-stone-900/90 hover:bg-[#fffdfa] dark:hover:bg-stone-900 rounded-2xl p-4 border-2 border-[#e6ded5] dark:border-stone-800 hover:border-[#702923] dark:hover:border-amber-500 shadow-md hover:shadow-xl transition-all duration-300 flex flex-col justify-between cursor-pointer"
        >
          <div>
            <!-- IMAGE CONTAINER -->
            <div class="relative w-full h-48 rounded-xl overflow-hidden mb-4 bg-stone-200 dark:bg-stone-800">
              <img 
                :src="getImageUrl(item.image)" 
                :alt="item.title" 
                class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-300"
              />
            </div>

            <!-- TITLE & DESCRIPTION -->
            <h3 class="text-sm sm:text-base font-black text-[#702923] dark:text-amber-400 line-clamp-3 group-hover:text-[#521d18] dark:group-hover:text-amber-300 transition-colors leading-snug text-center px-1">
              {{ item.title }}
            </h3>
          </div>

          <!-- CARD FOOTER (Date & Arrow Button) -->
          <div class="flex items-center justify-between pt-3 mt-4 border-t border-[#e2d7c7] dark:border-stone-800 text-stone-400">
            <!-- Arrow Indicator -->
            <div class="w-7 h-7 rounded-full bg-[#e8ded3] dark:bg-stone-800 group-hover:bg-[#702923] dark:group-hover:bg-amber-500 text-stone-500 dark:text-stone-300 group-hover:text-white dark:group-hover:text-stone-950 flex items-center justify-center transition-all">
              <Icon 
                :icon="currentLang === 'ar' ? 'mdi:chevron-left' : 'mdi:chevron-right'" 
                class="w-4 h-4" 
              />
            </div>

            <!-- Date -->
            <span class="text-xs font-bold text-stone-500 dark:text-stone-400">{{ item.date }}</span>
          </div>

        </div>
      </div>

    </div>
  </section>
</template>

<script>
import { Icon } from '@iconify/vue2';

export default {
  name: 'NewsSection',
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
  },
  methods: {
    // Helper method to resolve public assets correctly on any route path
    getImageUrl(path) {
      const baseUrl = process.env.BASE_URL || '/';
      const cleanPath = path.startsWith('/') ? path.slice(1) : path;
      return `${baseUrl}${cleanPath}`;
    }
  },
  computed: {
    localizedNews() {
      const isAr = this.currentLang === 'ar';
      return [
        {
          title: isAr 
            ? 'الهيئة العليا للحج والعمرة تُطلق الاستمارة الخاصة بـ "لم الشمل" و "تعديل البيانات" عبر بوابة أور الإلكترونية'
            : 'Hajj and Umrah Supreme Commission launches "Reunion" and "Data Modification" forms via Ur Portal',
          date: isAr ? '٢٩ يوليو ٢٠٢٦' : 'July 29, 2026',
          image: 'photo1.jpg'
        },
        {
          title: isAr 
            ? 'لضمان السرعة والأولوية في المتابعة... "بوابة أور" تطلق منصة "رسائلي" المباشرة للدعم الفني'
            : 'To ensure speed and priority... Ur Portal launches "Rasaeliy" direct support platform',
          date: isAr ? '٣٠ يوليو ٢٠٢٦' : 'July 30, 2026',
          image: 'photo4.png'
        },
        {
          title: isAr 
            ? 'الهيئة العليا للحج والعمرة تُطلق خدمة استرجاع مبالغ التسجيل لقرعة الحج إلكترونياً'
            : 'Hajj and Umrah Supreme Commission launches electronic refund service for Hajj lottery fees',
          date: isAr ? '١ أغسطس ٢٠٢٦' : 'August 1, 2026',
          image: 'photo3.png'
        },
        {
          title: isAr 
            ? 'هيئة التقاعد الوطنية تطلق استمارة تحديث بيانات المتقاعدين بالتنسيق مع المركز الوطني للتحول الرقمي'
            : 'National Retirement Board launches retiree data update form with the Digital Transformation Center',
          date: isAr ? '١٤ سبتمبر ٢٠٢٦' : 'September 14, 2026',
          image: 'photo2.jpg'
        }
      ];
    }
  }
};
</script>