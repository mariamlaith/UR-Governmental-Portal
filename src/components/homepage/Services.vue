<template>
  <section 
    :class="[
      'w-full px-4 sm:px-6 lg:px-8 py-6 font-sans transition-colors duration-200',
      isDarkMode ? 'dark' : ''
    ]" 
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <div class="bg-[#f4efe8]/90 dark:bg-stone-900/90 backdrop-blur-md rounded-2xl max-w-[1500px] mx-auto p-4 sm:p-6 lg:p-8 shadow-sm border border-[#e2d7c7] dark:border-stone-800 transition-colors">
      
      <!-- HEADER ROW -->
      <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 pb-5 border-b border-[#e2d7c7]/80 dark:border-stone-800 mb-6">
        <!-- Title & Subtitle -->
        <div class="flex items-center gap-3.5">
          <div class="p-3 bg-[#702923]/10 dark:bg-amber-500/10 text-[#702923] dark:text-amber-500 rounded-xl shrink-0">
            <Icon icon="mdi:grid-large" class="w-7 h-7" />
          </div>
          <div>
            <h2 class="text-xl sm:text-2xl font-black text-stone-900 dark:text-stone-100">
              {{ currentLang === 'ar' ? 'دليل الخدمات' : 'Services Directory' }}
            </h2>
            <p class="text-xs sm:text-sm text-stone-600 dark:text-stone-400 font-bold mt-0.5">
              {{ currentLang === 'ar' ? 'تصفح جميع الخدمات الحكومية حسب الفئة' : 'Browse all government services by category' }}
            </p>
          </div>
        </div>

        <!-- View All Link -->
        <a 
          href="#" 
          class="flex items-center gap-1.5 text-base font-extrabold text-[#702923] dark:text-amber-500 hover:text-[#521d18] dark:hover:text-amber-400 transition-colors self-end sm:self-auto"
        >
          <span>{{ currentLang === 'ar' ? 'اعرض جميع الخدمات' : 'View All Services' }}</span>
          <Icon 
            :icon="currentLang === 'ar' ? 'mdi:arrow-left' : 'mdi:arrow-right'" 
            class="w-4 h-4" 
          />
        </a>
      </div>

      <!-- 12-CARD GRID -->
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-3 sm:gap-4 lg:gap-5">
        <div 
          v-for="(service, index) in localizedServices" 
          :key="index"
          class="group relative bg-[#faf7f2] dark:bg-stone-800/80 hover:bg-[#fffdfa] dark:hover:bg-stone-800 rounded-2xl p-4 sm:p-5 border-2 border-[#e6ded5] dark:border-stone-700/70 hover:border-[#702923] dark:hover:border-amber-500 shadow-md hover:shadow-xl transition-all duration-300 flex flex-col items-center text-center cursor-pointer min-h-[170px] justify-between"
        >
          <!-- Icon inside soft circle -->
          <div class="w-12 h-12 sm:w-14 sm:h-14 rounded-full bg-[#f0e8df] dark:bg-stone-700/60 group-hover:bg-[#702923]/10 dark:group-hover:bg-amber-500/20 flex items-center justify-center text-[#702923] dark:text-amber-400 transition-colors shrink-0">
            <Icon :icon="service.icon" class="w-6 h-6 sm:w-7 sm:h-7" />
          </div>

          <!-- Titles -->
          <div class="my-2">
            <h3 class="text-sm sm:text-base font-black text-stone-800 dark:text-stone-100 group-hover:text-[#702923] dark:group-hover:text-amber-400 transition-colors leading-tight">
              {{ service.title }}
            </h3>
            <p class="text-[11px] sm:text-xs text-stone-500 dark:text-stone-400 font-bold mt-1 leading-snug">
              {{ service.subtitle }}
            </p>
          </div>

          <!-- Arrow Indicator -->
          <div class="w-6 h-6 rounded-full bg-[#e8ded3] dark:bg-stone-700 group-hover:bg-[#702923] dark:group-hover:bg-amber-500 text-stone-500 dark:text-stone-300 group-hover:text-white dark:group-hover:text-stone-950 flex items-center justify-center transition-all">
            <Icon 
              :icon="currentLang === 'ar' ? 'mdi:chevron-left' : 'mdi:chevron-right'" 
              class="w-4 h-4" 
            />
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script>
import { Icon } from '@iconify/vue2';

export default {
  name: 'ServicesGrid',
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
  computed: {
    localizedServices() {
      const isAr = this.currentLang === 'ar';
      return [
        {
          title: isAr ? 'التقاعد' : 'Retirement',
          subtitle: isAr ? 'خدمات المتقاعدين' : 'Retiree Services',
          icon: 'mdi:account-group'
        },
        {
          title: isAr ? 'الضرائب' : 'Taxes',
          subtitle: isAr ? 'الاستعلام والدفع' : 'Inquiry & Payment',
          icon: 'mdi:cash-register'
        },
        {
          title: isAr ? 'الجوازات والسفر' : 'Passports & Travel',
          subtitle: isAr ? 'إصدار أو تجديد' : 'Issue or Renew',
          icon: 'mdi:passport'
        },
        {
          title: isAr ? 'الإسكان والمشاريع' : 'Housing & Projects',
          subtitle: isAr ? 'خدمات الإسكان' : 'Housing Services',
          icon: 'mdi:home-city'
        },
        {
          title: isAr ? 'المرور والمركبات' : 'Traffic & Vehicles',
          subtitle: isAr ? 'تسجيل ودفع الرسوم' : 'Registration & Fees',
          icon: 'mdi:car'
        },
        {
          title: isAr ? 'البطاقة الوطنية' : 'National ID',
          subtitle: isAr ? 'إصدار أو تجديد' : 'Issue or Renew',
          icon: 'mdi:card-account-details'
        },
        {
          title: isAr ? 'الثقافة والسياحة' : 'Culture & Tourism',
          subtitle: isAr ? 'الآثار والمواقع السياحية' : 'Heritage & Tourism',
          icon: 'mdi:bank'
        },
        {
          title: isAr ? 'الاقتصاد والمالية' : 'Economy & Finance',
          subtitle: isAr ? 'الاستثمار والترخيص' : 'Investment & Licensing',
          icon: 'mdi:chart-line'
        },
        {
          title: isAr ? 'العمل والشؤون الاجتماعية' : 'Labor & Social Affairs',
          subtitle: isAr ? 'خدمات التوظيف والرعاية' : 'Employment & Welfare',
          icon: 'mdi:briefcase-account'
        },
        {
          title: isAr ? 'الزراعة والثروة الحيوانية' : 'Agriculture & Livestock',
          subtitle: isAr ? 'دعم وتنمية' : 'Support & Growth',
          icon: 'mdi:sprout'
        },
        {
          title: isAr ? 'الصحة' : 'Health',
          subtitle: isAr ? 'المستشفيات والخدمات' : 'Hospitals & Care',
          icon: 'mdi:hospital-building'
        },
        {
          title: isAr ? 'التعليم' : 'Education',
          subtitle: isAr ? 'القبول والمنح' : 'Admissions & Grants',
          icon: 'mdi:school'
        }
      ];
    }
  }
};
</script>