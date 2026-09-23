<template>
  <header
    :class="[
      'sticky top-0 z-50 w-full border-b font-sans transition-colors duration-200',
      isDarkMode
        ? 'border-stone-800 bg-stone-950/95 text-stone-100'
        : 'border-[#e8ddd3] bg-[#F5EDE2]/100 text-[#33231d]'
    ]"
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <div class="mx-auto max-w-[1440px] px-5 sm:px-8 lg:px-12">
      <div
    class="flex h-8 items-center justify-start border-b text-xs font-bold sm:text-sm" 
      :class="isDarkMode ? 'border-stone-800 text-stone-400' : 'border-[#eee5de] text-[#6f625a]'"
      >
        
        <div class="flex items-center gap-3">
          <div class="flex items-center gap-1" :aria-label="currentLang === 'ar' ? 'حجم الخط' : 'Font size'">
            <button @click="changeFontSize('small')" class="hover:text-[#702923]" title="Font Small">A-</button>
            <button @click="changeFontSize('normal')" class="hover:text-[#702923]" title="Font Default">A</button>
            <button @click="changeFontSize('large')" class="hover:text-[#702923]" title="Font Large">A+</button>
          </div>
          <span class="h-4 w-px" :class="isDarkMode ? 'bg-stone-700' : 'bg-[#d9ccc2]'" />
          <button @click="toggleDarkMode" class="flex items-center gap-1 transition-colors hover:text-[#702923]">
            <Icon :icon="isDarkMode ? 'mdi:weather-sunny' : 'mdi:weather-night'" class="h-4 w-4" />
            <span class="hidden sm:inline">{{ isDarkMode ? 'Light' : 'Dark' }}</span>
          </button>
          <button @click="toggleLanguage" class="flex items-center gap-1 transition-colors hover:text-[#702923]">
            <Icon icon="mdi:web" class="h-4 w-4" />
            <span>{{ currentLang === 'ar' ? 'English' : 'العربية' }}</span>
          </button>
        </div>
      </div>

      <div class="relative flex min-h-[58px] items-center justify-between gap-5 py-1">
        <a href="#" class="flex shrink-0 items-center" aria-label="Ur Portal">
          <img src="/urlogobg.png" alt="بوابة أور" class="h-[5rem] w-auto object-contain sm:h-[5.75rem]" />
        </a>

        <nav class="hidden flex-1 items-center justify-center gap-5 text-base font-bold xl:flex" aria-label="Main navigation">
          <a href="#" class="relative whitespace-nowrap py-4 text-[#702923] after:absolute after:inset-x-0 after:bottom-0 after:h-0.5 after:bg-[#702923]">
            {{ currentLang === 'ar' ? 'الرئيسية' : 'Home' }}
          </a>
          <a href="#" class="nav-link">{{ currentLang === 'ar' ? 'الخدمات' : 'Services' }}</a>
          <a href="#" class="nav-link">{{ currentLang === 'ar' ? 'من نحن' : 'About Us' }} <Icon icon="mdi:chevron-down" class="h-3 w-3" /></a>
          <a href="#" class="nav-link">{{ currentLang === 'ar' ? 'الأخبار' : 'News' }} <Icon icon="mdi:chevron-down" class="h-3 w-3" /></a>
          <a href="#" class="nav-link">{{ currentLang === 'ar' ? 'المواقع الحكومية' : 'Government Sites' }} <Icon icon="mdi:chevron-down" class="h-3 w-3" /></a>
          <a href="#" class="nav-link">{{ currentLang === 'ar' ? 'الاستفسارات' : 'Inquiries' }} <Icon icon="mdi:chevron-down" class="h-3 w-3" /></a>
          <a href="#" class="nav-link">{{ currentLang === 'ar' ? 'الأسئلة الشائعة' : 'FAQs' }}</a>
        </nav>
        <router-link to="/Login"   class="flex shrink-0 items-center gap-2 rounded-full bg-[#702923] px-4 py-2 text-xs font-bold text-white shadow-sm transition-colors hover:bg-[#57201c] sm:px-5 sm:text-sm" type="button">
            <span>{{ currentLang === 'ar' ? 'تسجيل الدخول' : 'Sign In' }}</span>
            <Icon icon="mdi:account-outline" class="h-4 w-4" />
        </router-link>

        <button
          @click="isMobileMenuOpen = !isMobileMenuOpen"
          class="rounded-md p-2 text-[#702923] xl:hidden"
          :aria-label="currentLang === 'ar' ? 'فتح القائمة' : 'Open menu'"
        >
          <Icon :icon="isMobileMenuOpen ? 'mdi:close' : 'mdi:menu'" class="h-7 w-7" />
        </button>
      </div>

      <nav v-if="isMobileMenuOpen" class="flex flex-col gap-1 border-t py-3 text-sm font-bold xl:hidden" :class="isDarkMode ? 'border-stone-800' : 'border-[#eee5de]'" aria-label="Mobile navigation">
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'الرئيسية' : 'Home' }}</a>
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'الخدمات' : 'Services' }}</a>
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'من نحن' : 'About Us' }}</a>
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'الأخبار' : 'News' }}</a>
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'المواقع الحكومية' : 'Government Sites' }}</a>
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'الاستفسارات' : 'Inquiries' }}</a>
        <a href="#" class="mobile-link">{{ currentLang === 'ar' ? 'الأسئلة الشائعة' : 'FAQs' }}</a>
      </nav>
    </div>
  </header>
</template>

<script>
import { Icon } from '@iconify/vue2'

export default {
  name: 'AppHeader',
  components: { Icon },
  props: {
    isDarkMode: { type: Boolean, default: false },
    currentLang: { type: String, default: 'ar' }
  },
  data() {
    return { isMobileMenuOpen: false }
  },
  methods: {
    toggleDarkMode() {
      this.$emit('toggle-dark-mode')
    },
    toggleLanguage() {
      this.$emit('toggle-language')
    },
    changeFontSize(size) {
      const root = document.documentElement
      if (size === 'small') root.style.fontSize = '14px'
      if (size === 'normal') root.style.fontSize = '16px'
      if (size === 'large') root.style.fontSize = '18px'
    }
  }
}
</script>

<style scoped>
.nav-link {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  white-space: nowrap;
  padding-top: 1rem;
  padding-bottom: 1rem;
  transition: color 0.2s ease;
}

.nav-link:hover,
.mobile-link:hover {
  color: #702923;
}

.mobile-link {
  padding: 0.55rem 0.25rem;
  transition: color 0.2s ease;
}
</style>
