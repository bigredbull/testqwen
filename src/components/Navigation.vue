<template>
  <div class="nav-categories">
    <div class="container">
      <h2>热门分类</h2>
      <ul class="category-list">
        <li v-for="category in categories" :key="category.id">
          <a :href="`#${category.id}`" class="category-link">
            {{ category.name }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  props: {
    categories: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.nav-categories {
    background: white;
    padding: 1.5rem 0;
    border-bottom: 1px solid #eee;
}

.nav-categories h2 {
    text-align: center;
    margin-bottom: 1rem;
    font-size: 1.2rem;
    color: #333;
}

.category-list {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 1rem;
    list-style: none;
}

.category-list li {
    list-style: none;
}

.category-link {
    display: inline-block;
    padding: 8px 16px;
    background: #f0f2f5;
    color: #333;
    text-decoration: none;
    border-radius: 20px;
    transition: all 0.3s ease;
}

.category-link:hover {
    background: #667eea;
    color: white;
    transform: translateY(-2px);
}
</style>
