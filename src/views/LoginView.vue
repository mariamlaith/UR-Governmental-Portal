<template>
  <div 
    :class="[
      'home-page font-sans min-h-screen transition-colors duration-200',
      isDarkMode ? 'dark bg-stone-950 text-stone-100' : 'bg-[#faf7f2] text-stone-900'
    ]"
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >

      <Login 
        :is-dark-mode="isDarkMode" 
        :current-lang="currentLang" 
      />
  </div>
  
</template>

<script>
import Login from '@/components/Login.vue'

export default {
  name: 'LoginView',
  components: {
    Login,
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