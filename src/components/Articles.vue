<template>
  <section id="articles" class="articles">
    <div class="articles-container">
      <h2 class="section-title">最新文章</h2>
      <div class="articles-grid">
        <article class="article-card">
          <div class="article-header purple"></div>
          <div class="article-content">
            <div class="article-meta">
              <span class="article-tag purple-tag">React</span>
              <span class="article-date">2024-01-15</span>
            </div>
            <h3 class="article-title">React Hooks最佳实践指南</h3>
            <p class="article-description">
              深入探讨React Hooks的使用技巧和常见陷阱, 帮助开发者写出更优雅的代码。
            </p>
            <div class="article-footer">
              <div class="article-stats">
                <span class="stat-item">👁️ 1.2k</span>
                <span class="stat-item">💬 23</span>
                <span class="stat-item">❤️ 89</span>
              </div>
              <a href="#" class="read-more purple-link">阅读更多</a>
            </div>
          </div>
        </article>
        <article class="article-card">
          <div class="article-header blue"></div>
          <div class="article-content">
            <div class="article-meta">
              <span class="article-tag blue-tag">CSS</span>
              <span class="article-date">2024-01-10</span>
            </div>
            <h3 class="article-title">CSS Grid布局完全指南</h3>
            <p class="article-description">
              从基础到高级,全面介绍CSS Grid的使用方法和实际应用场景。
            </p>
            <div class="article-footer">
              <div class="article-stats">
                <span class="stat-item">👁️ 856</span>
                <span class="stat-item">💬 15</span>
                <span class="stat-item">❤️ 67</span>
              </div>
              <a href="#" class="read-more blue-link">阅读更多</a>
            </div>
          </div>
        </article>
        <article class="article-card">
          <div class="article-header green"></div>
          <div class="article-content">
            <div class="article-meta">
              <span class="article-tag green-tag">性能</span>
              <span class="article-date">2024-01-05</span>
            </div>
            <h3 class="article-title">前端性能优化实战</h3>
            <p class="article-description">
              分享一些实用的前端性能优化技巧,让你的网站飞起来。
            </p>
            <div class="article-footer">
              <div class="article-stats">
                <span class="stat-item">👁️ 2.1k</span>
                <span class="stat-item">💬 45</span>
                <span class="stat-item">❤️ 156</span>
              </div>
              <a href="#" class="read-more green-link">阅读更多</a>
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.articles {
  background-color: #F8F8F8;
  padding: 6rem 2rem;
}

.articles-container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  font-size: 3rem;
  text-align: center;
  margin-bottom: 4rem;
  color: #333;
  font-weight: bold;
}

.articles-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.article-card {
  background-color: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.article-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.article-header {
  height: 120px;
  width: 100%;
}

.article-header.purple {
  background-color: rgb(178, 61, 206);
}

.article-header.blue {
  background-color: #4169E1;
}

.article-header.green {
  background-color: #32CD32;
}

.article-content {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.article-meta {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.article-tag {
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 500;
  color: white;
}

.purple-tag {
  background-color: rgb(200, 100, 230);
}

.blue-tag {
  background-color: #6495ED;
}

.green-tag {
  background-color: #90EE90;
}

.article-date {
  font-size: 0.85rem;
  color: #999;
}

.article-title {
  font-size: 1.3rem;
  font-weight: bold;
  color: #333;
  margin: 0;
}

.article-description {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.6;
  margin: 0;
}

.article-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 1rem;
}

.article-stats {
  display: flex;
  gap: 1rem;
  font-size: 0.85rem;
  color: #999;
}

.stat-item {
  display: flex;
  align-items: center;
  gap: 0.25rem;
}

.read-more {
  font-size: 0.95rem;
  font-weight: 500;
  text-decoration: none;
  transition: opacity 0.3s;
}

.read-more:hover {
  opacity: 0.8;
}

.purple-link {
  color: rgb(178, 61, 206);
}

.blue-link {
  color: #4169E1;
}

.green-link {
  color: #32CD32;
}

@media (max-width: 968px) {
  .articles-grid {
    grid-template-columns: 1fr;
  }
  
  .section-title {
    font-size: 2rem;
  }
}
</style>

