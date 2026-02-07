<template>
  <div id="app">
    <Header />
    <SearchBar />
    <Navigation :categories="categories" />
    <MainContent :categories="categories" />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import SearchBar from './components/SearchBar.vue'
import Navigation from './components/Navigation.vue'
import MainContent from './components/MainContent.vue'
import Footer from './components/Footer.vue'
import { categories } from './data/categories'

export default {
  name: 'App',
  components: {
    Header,
    SearchBar,
    Navigation,
    MainContent,
    Footer
  },
  data() {
    return {
      categories
    }
  }
}
</script>

<style scoped>
#app {
  width: 100%;
}
</style>
