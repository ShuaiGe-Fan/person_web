<template>
  <section id="about" class="about">
    <div class="about-container">
      <h2 class="section-title">关于我</h2>
      <div class="about-content">
        <div class="about-story">
          <h3 class="story-title">我的故事</h3>
          <p class="story-text">
            我是一名充满激情的前端开发工程师,拥有5年的Web开发经验。专注于React生态系统,热爱创造直观且美观的用户界面。
          </p>
          <p class="story-text">
            在我的职业生涯中,我参与了多个大型项目的开发,从电商平台到企业级应用,积累了丰富的实战经验。
          </p>
          <div class="stats">
            <div class="stat-item">
              <div class="stat-number">5+</div>
              <div class="stat-label">年工作经验</div>
            </div>
            <div class="stat-item">
              <div class="stat-number">50+</div>
              <div class="stat-label">完成项目</div>
            </div>
            <div class="stat-item">
              <div class="stat-number">20+</div>
              <div class="stat-label">技术文章</div>
            </div>
          </div>
        </div>
        <div class="about-education">
          <h3 class="education-title">教育背景</h3>
          <div class="education-list">
            <div class="education-item">
              <div class="education-icon">🎓</div>
              <div class="education-content">
                <div class="education-degree">计算机科学学士</div>
                <div class="education-school">清华大学 • 2016-2020</div>
              </div>
            </div>
            <div class="education-item">
              <div class="education-icon">📜</div>
              <div class="education-content">
                <div class="education-degree">前端工程师认证</div>
                <div class="education-school">阿里云 • 2021</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.about {
  background-color: #ffffff;
  padding: 6rem 2rem;
}

.about-container {
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

.about-content {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 4rem;
}

.about-story {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.story-title {
  font-size: 2rem;
  color: #8A2BE2;
  margin: 0;
  font-weight: bold;
}

.story-text {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #555;
  margin: 0;
}

.stats {
  display: flex;
  gap: 3rem;
  margin-top: 2rem;
}

.stat-item {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.stat-number {
  font-size: 2.5rem;
  font-weight: bold;
  color: #8A2BE2;
}

.stat-label {
  font-size: 1rem;
  color: #777;
}

.about-education {
  background-color: #F5F5F5;
  padding: 2rem;
  border-radius: 12px;
}

.education-title {
  font-size: 1.5rem;
  color: #333;
  margin: 0 0 1.5rem 0;
  font-weight: bold;
}

.education-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.education-item {
  display: flex;
  gap: 1rem;
  align-items: flex-start;
}

.education-icon {
  font-size: 2rem;
  color: #8A2BE2;
  flex-shrink: 0;
}

.education-content {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.education-degree {
  font-size: 1.1rem;
  font-weight: 600;
  color: #333;
}

.education-school {
  font-size: 0.95rem;
  color: #777;
}

@media (max-width: 968px) {
  .about-content {
    grid-template-columns: 1fr;
  }
  
  .stats {
    justify-content: space-around;
  }
  
  .section-title {
    font-size: 2rem;
  }
}
</style>

