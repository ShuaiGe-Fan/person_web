<template>
  <section id="tech" class="tech-stack">
    <div class="tech-container">
      <h2 class="section-title">技术栈</h2>
      <div class="tech-cards">
        <div class="tech-card">
          <div class="tech-icon frontend-icon">⚛️</div>
          <h3 class="tech-category">前端框架</h3>
          <div class="skill-list">
            <div class="skill-item">
              <div class="skill-header">
                <span class="skill-name">React</span>
                <span class="skill-percent">95%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 95%"></div>
              </div>
            </div>
            <div class="skill-item">
              <div class="skill-header">
                <span class="skill-name">Vue.js</span>
                <span class="skill-percent">85%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 85%"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="tech-card">
          <div class="tech-icon language-icon">JS</div>
          <h3 class="tech-category">编程语言</h3>
          <div class="skill-list">
            <div class="skill-item">
              <div class="skill-header">
                <span class="skill-name">JavaScript</span>
                <span class="skill-percent">90%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 90%"></div>
              </div>
            </div>
            <div class="skill-item">
              <div class="skill-header">
                <span class="skill-name">TypeScript</span>
                <span class="skill-percent">80%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 80%"></div>
              </div>
            </div>
          </div>
        </div>
        <div class="tech-card">
          <div class="tech-icon tools-icon">🔧</div>
          <h3 class="tech-category">开发工具</h3>
          <div class="skill-list">
            <div class="skill-item">
              <div class="skill-header">
                <span class="skill-name">Git</span>
                <span class="skill-percent">90%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 90%"></div>
              </div>
            </div>
            <div class="skill-item">
              <div class="skill-header">
                <span class="skill-name">Webpack</span>
                <span class="skill-percent">75%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 75%"></div>
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
.tech-stack {
  background-color: #F8F8F8;
  padding: 6rem 2rem;
}

.tech-container {
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

.tech-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.tech-card {
  background-color: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.tech-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.tech-icon {
  width: 60px;
  height: 60px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  margin-bottom: 1rem;
}

.frontend-icon {
  background-color: #E3F2FD;
}

.language-icon {
  background-color: #FFF9C4;
  font-weight: bold;
  font-size: 1.5rem;
  color: #333;
}

.tools-icon {
  background-color: #E8F5E9;
}

.tech-category {
  font-size: 1.3rem;
  color: #333;
  margin: 0 0 1.5rem 0;
  font-weight: 600;
}

.skill-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skill-item {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.skill-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.skill-name {
  font-size: 1rem;
  color: #333;
  font-weight: 500;
}

.skill-percent {
  font-size: 0.9rem;
  color: #777;
}

.skill-bar {
  width: 100%;
  height: 8px;
  background-color: #E0E0E0;
  border-radius: 4px;
  overflow: hidden;
}

.skill-progress {
  height: 100%;
  background-color: #8A2BE2;
  border-radius: 4px;
  transition: width 0.3s;
}

@media (max-width: 968px) {
  .tech-cards {
    grid-template-columns: 1fr;
  }
  
  .section-title {
    font-size: 2rem;
  }
}
</style>

