<template>
  <header class="header">
    <div class="header-container">
      <div class="logo">
        <!-- <span class="logo-icon">&lt;/&gt;</span> -->
        <span class="logo-text">飞飞公主</span>
      </div>
      <nav class="nav">
        <a href="#home" class="nav-link" @click.prevent="scrollTo('#home')">首页</a>
        <a href="#about" class="nav-link" @click.prevent="scrollTo('#about')">关于我</a>
        <a href="#tech" class="nav-link" @click.prevent="scrollTo('#tech')">技术栈</a>
        <a href="#interests" class="nav-link" @click.prevent="scrollTo('#interests')">兴趣爱好</a>
        <a href="#articles" class="nav-link" @click.prevent="scrollTo('#articles')">文章</a>
        <a href="#contact" class="nav-link" @click.prevent="scrollTo('#contact')">联系我</a>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
const scrollTo = (selector: string) => {
  const element = document.querySelector(selector)
  if (element) {
    const headerHeight = 80
    const elementPosition = element.getBoundingClientRect().top + window.pageYOffset
    const offsetPosition = elementPosition - headerHeight

    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    })
  }
}
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  background-color: rgba(138, 43, 226, 0.95);
  backdrop-filter: blur(10px);
}

.header-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: white;
  font-size: 1.5rem;
  font-weight: bold;
}

.logo-icon {
  font-size: 1.8rem;
}

.logo-text {
  font-weight: 600;
}

.nav {
  display: flex;
  gap: 2rem;
}

.nav-link {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  transition: opacity 0.3s;
  cursor: pointer;
}

.nav-link:hover {
  opacity: 0.8;
}

@media (max-width: 768px) {
  .header-container {
    padding: 1rem;
  }
  
  .nav {
    gap: 1rem;
    flex-wrap: wrap;
  }
  
  .nav-link {
    font-size: 0.9rem;
  }
}
</style>

