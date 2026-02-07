<template>
  <div class="header">
    <div class="container">
      <h1>AI导航</h1>
      <p>发现最好的人工智能资源与工具</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 2rem 0;
    text-align: center;
}

.header h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
}

.header p {
    font-size: 1.1rem;
    opacity: 0.9;
}

@media (max-width: 768px) {
    .header h1 {
        font-size: 2rem;
    }
}
</style>
