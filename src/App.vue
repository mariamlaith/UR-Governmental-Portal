<template>
  <div
    id="app"
    :class="[
      'min-h-screen flex flex-col justify-between transition-colors duration-200',
      isDarkMode ? 'dark bg-stone-950 text-stone-100' : 'bg-stone-50 text-stone-800'
    ]"
    :dir="currentLang === 'ar' ? 'rtl' : 'ltr'"
  >
    <!-- Header Component -->
    <AppHeader
      :is-dark-mode="isDarkMode"
      :current-lang="currentLang"
      @toggle-dark-mode="toggleDarkMode"
      @toggle-language="toggleLanguage"
    />

    <!-- Main Dynamic View -->
    <main class="flex-grow">
      <router-view
        :is-dark-mode="isDarkMode"
        :current-lang="currentLang"
      />
    </main>

    <!-- Footer Component -->
    <AppFooter
      :is-dark-mode="isDarkMode"
      :current-lang="currentLang"
    />
  </div>
</template>

<script>
import AppHeader from './components/Layout/AppHeader.vue'
import AppFooter from './components/Layout/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter
  },
  data() {
    return {
      isDarkMode: false,
      currentLang: 'ar'
    }
  },
  watch: {
    isDarkMode: 'updateDocumentSettings',
    currentLang: 'updateDocumentSettings'
  },
  mounted() {
    this.updateDocumentSettings()
  },
  methods: {
    toggleDarkMode() {
      this.isDarkMode = !this.isDarkMode
    },
    toggleLanguage() {
      this.currentLang = this.currentLang === 'ar' ? 'en' : 'ar'
    },
    updateDocumentSettings() {
      document.documentElement.classList.toggle('dark', this.isDarkMode)
      document.documentElement.setAttribute('dir', this.currentLang === 'ar' ? 'rtl' : 'ltr')
      document.documentElement.setAttribute('lang', this.currentLang)
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
