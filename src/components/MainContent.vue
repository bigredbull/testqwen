<template>
  <div class="main-content">
    <div class="container">
      <CategorySection
        v-for="category in categories"
        :key="category.id"
        :category="category"
      />
    </div>
  </div>
</template>

<script>
import CategorySection from './CategorySection.vue'

export default {
  name: 'MainContent',
  components: {
    CategorySection
  },
  props: {
    categories: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.main-content {
    padding: 2rem 0;
}
</style>
