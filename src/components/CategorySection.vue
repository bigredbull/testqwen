<template>
  <div class="category-section" :id="category.id">
    <h3>{{ category.name }}</h3>
    <div class="links-grid">
      <LinkItem
        v-for="item in category.items"
        :key="item.title"
        :item="item"
      />
    </div>
  </div>
</template>

<script>
import LinkItem from './LinkItem.vue'

export default {
  name: 'CategorySection',
  components: {
    LinkItem
  },
  props: {
    category: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.category-section {
    margin-bottom: 3rem;
    scroll-margin-top: 80px;
}

.category-section h3 {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
    color: #333;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid #667eea;
    display: inline-block;
}

.links-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1.5rem;
}

@media (max-width: 768px) {
    .links-grid {
        grid-template-columns: 1fr;
    }
}
</style>
