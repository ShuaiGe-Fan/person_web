<template>
  <section id="interests" class="interests">
    <div class="interests-container">
      <h2 class="section-title">兴趣爱好</h2>
      <div class="interests-grid">
        <div class="interest-item">
          <div class="interest-icon">📷</div>
          <h3 class="interest-name">摄影</h3>
          <p class="interest-description">
            热爱捕捉生活中的美好瞬间,擅长风景和人像摄影
          </p>
        </div>
        <div class="interest-item">
          <div class="interest-icon">🎵</div>
          <h3 class="interest-name">音乐</h3>
          <p class="interest-description">
            喜欢听各种类型的音乐,偶尔也会弹吉他放松心情
          </p>
        </div>
        <div class="interest-item">
          <div class="interest-icon">✈️</div>
          <h3 class="interest-name">旅行</h3>
          <p class="interest-description">
            探索不同的文化和风景,寻找设计灵感
          </p>
        </div>
        <div class="interest-item">
          <div class="interest-icon">📚</div>
          <h3 class="interest-name">阅读</h3>
          <p class="interest-description">
            技术书籍和小说都爱看,持续学习新知识
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.interests {
  background-color: #ffffff;
  padding: 6rem 2rem;
}

.interests-container {
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

.interests-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2rem;
}

.interest-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 1rem;
}

.interest-icon {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background-color: #E1BEE7;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 3rem;
  margin-bottom: 0.5rem;
}

.interest-name {
  font-size: 1.3rem;
  color: #333;
  margin: 0;
  font-weight: 600;
}

.interest-description {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.6;
  margin: 0;
}

@media (max-width: 968px) {
  .interests-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .section-title {
    font-size: 2rem;
  }
}

@media (max-width: 600px) {
  .interests-grid {
    grid-template-columns: 1fr;
  }
}
</style>

