<template>
  <div class="search-bar">
    <div class="container">
      <form @submit.prevent="handleSearch">
        <input
          v-model="searchQuery"
          type="text"
          placeholder="搜索AI相关资源..."
        >
        <button type="submit">搜索</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  data() {
    return {
      searchQuery: ''
    }
  },
  methods: {
    handleSearch() {
      if (this.searchQuery.trim()) {
        const searchUrl = `https://www.google.com/search?q=${encodeURIComponent(this.searchQuery)}`;
        window.open(searchUrl, '_blank');
      }
    }
  }
}
</script>

<style scoped>
.search-bar {
    background: white;
    padding: 2rem 0;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

.search-bar form {
    display: flex;
    max-width: 600px;
    margin: 0 auto;
}

.search-bar input {
    flex: 1;
    padding: 12px 15px;
    border: 2px solid #ddd;
    border-radius: 25px 0 0 25px;
    font-size: 1rem;
    outline: none;
    transition: border-color 0.3s ease;
}

.search-bar input:focus {
    border-color: #667eea;
}

.search-bar button {
    padding: 12px 20px;
    background: #667eea;
    color: white;
    border: none;
    border-radius: 0 25px 25px 0;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.3s ease;
}

.search-bar button:hover {
    background: #764ba2;
}

@media (max-width: 768px) {
    .search-bar form {
        flex-direction: column;
        gap: 10px;
    }

    .search-bar input {
        border-radius: 25px;
    }

    .search-bar button {
        border-radius: 25px;
    }
}
</style>
