<template>
  <div id="app" class="min-h-screen bg-stone-50 text-stone-800 flex flex-col justify-between">
    <!-- Header Component -->
    <AppHeader />

    <!-- Main Dynamic View -->
    <main class="flex-grow">
      <router-view />
    </main>

    <!-- Footer Component -->
    <AppFooter />
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
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
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
