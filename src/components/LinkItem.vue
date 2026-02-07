<template>
  <a :href="item.url" target="_blank" class="link-item">
    <div class="link-icon">{{ item.icon }}</div>
    <div class="link-info">
      <h4>{{ item.title }}</h4>
      <p>{{ item.description }}</p>
    </div>
  </a>
</template>

<script>
export default {
  name: 'LinkItem',
  props: {
    item: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.link-item {
    display: flex;
    align-items: center;
    background: white;
    padding: 1rem;
    border-radius: 10px;
    text-decoration: none;
    color: inherit;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.link-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 20px rgba(0,0,0,0.15);
}

.link-icon {
    font-size: 2rem;
    margin-right: 1rem;
    flex-shrink: 0;
}

.link-info h4 {
    color: #333;
    margin-bottom: 0.5rem;
    font-size: 1rem;
    font-weight: 600;
}

.link-info p {
    color: #666;
    font-size: 0.9rem;
    margin: 0;
}

@media (max-width: 768px) {
    .link-item {
        flex-direction: row;
    }
}
</style>
