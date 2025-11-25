<template>
  <section id="home" class="hero">
    <div class="hero-container">
      <div class="hero-content">
        <h1 class="hero-title">你好,我是 飞飞公主</h1>
        <h2 class="hero-subtitle">前端开发工程师 | React专家 | UI/UX爱好者</h2>
        <p class="hero-description">
          专注于创建优雅、高性能的Web应用程序。热爱编程,追求完美的用户体验。
        </p>
        <div class="hero-buttons">
          <button class="btn btn-primary">查看作品</button>
          <button class="btn btn-outline">下载简历</button>
        </div>
      </div>
      <div class="hero-image">
        <div class="avatar-placeholder">
          <svg width="200" height="200" viewBox="0 0 200 200" fill="none">
            <circle cx="100" cy="100" r="100" fill="#E0E0E0"/>
            <circle cx="100" cy="80" r="30" fill="#9E9E9E"/>
            <path d="M 50 150 Q 100 120 150 150" stroke="#9E9E9E" stroke-width="20" fill="none" stroke-linecap="round"/>
          </svg>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.hero {
  background: linear-gradient(135deg, rgb(178, 61, 206) 0%, rgb(200, 100, 230) 100%);
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding-top: 80px;
  color: white;
}

.hero-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 4rem 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.hero-content {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: bold;
  margin: 0;
  line-height: 1.2;
}

.hero-subtitle {
  font-size: 1.5rem;
  font-weight: 500;
  margin: 0;
  opacity: 0.95;
}

.hero-description {
  font-size: 1.1rem;
  line-height: 1.6;
  margin: 0;
  opacity: 0.9;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}

.btn {
  padding: 0.875rem 2rem;
  font-size: 1rem;
  border-radius: 8px;
  border: none;
  cursor: pointer;
  font-weight: 500;
  transition: all 0.3s;
}

.btn-primary {
  background-color: rgb(178, 61, 206);
  color: white;
  border: 2px solid white;
}

.btn-primary:hover {
  background-color: white;
  color: rgb(178, 61, 206);
}

.btn-outline {
  background-color: transparent;
  color: white;
  border: 2px solid white;
}

.btn-outline:hover {
  background-color: white;
  color: rgb(178, 61, 206);
}

.hero-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.avatar-placeholder {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

@media (max-width: 968px) {
  .hero-container {
    grid-template-columns: 1fr;
    text-align: center;
  }
  
  .hero-title {
    font-size: 2.5rem;
  }
  
  .hero-subtitle {
    font-size: 1.2rem;
  }
  
  .avatar-placeholder {
    width: 200px;
    height: 200px;
  }
}
</style>

