<template>
  <section id="contact" class="contact">
    <div class="contact-container">
      <h2 class="contact-title">联系我</h2>
      <div class="contact-content">
        <div class="contact-info">
          <h3 class="info-title">让我们一起创造些什么</h3>
          <p class="info-description">
            如果你有有趣的项目想要合作,或者想要交流技术问题,随时联系我。我很乐意与志同道合的人一起工作。
          </p>
          <div class="contact-details">
            <div class="contact-detail-item">
              <span class="contact-icon">✉️</span>
              <span class="contact-text">feifei.princess@example.com</span>
            </div>
            <div class="contact-detail-item">
              <span class="contact-icon">📱</span>
              <span class="contact-text">+86 138 0000 0000</span>
            </div>
            <div class="contact-detail-item">
              <span class="contact-icon">📍</span>
              <span class="contact-text">北京, 中国</span>
            </div>
          </div>
        </div>
        <div class="contact-form-wrapper">
          <form class="contact-form" @submit.prevent="submitForm">
            <div class="form-group">
              <label class="form-label">姓名</label>
              <input
                v-model="form.name"
                type="text"
                placeholder="你的姓名"
                class="form-input"
                required
              />
            </div>
            <div class="form-group">
              <label class="form-label">邮箱</label>
              <input
                v-model="form.email"
                type="email"
                placeholder="你的邮箱"
                class="form-input"
                required
              />
            </div>
            <div class="form-group">
              <label class="form-label">消息</label>
              <textarea
                v-model="form.message"
                placeholder="你想说什么..."
                class="form-textarea"
                rows="5"
                required
              ></textarea>
            </div>
            <button type="submit" class="submit-button">发送消息</button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const submitForm = () => {
  if (form.name && form.email && form.message) {
    alert('消息已发送！感谢您的联系。')
    form.name = ''
    form.email = ''
    form.message = ''
  }
}
</script>

<style scoped>
.contact {
  background: linear-gradient(135deg, #8A2BE2 0%, #9370DB 100%);
  padding: 6rem 2rem;
  color: white;
}

.contact-container {
  max-width: 1200px;
  margin: 0 auto;
}

.contact-title {
  font-size: 3rem;
  text-align: center;
  margin-bottom: 4rem;
  color: white;
  font-weight: bold;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.info-title {
  font-size: 2rem;
  margin: 0;
  font-weight: 600;
}

.info-description {
  font-size: 1.1rem;
  line-height: 1.8;
  margin: 0;
  opacity: 0.95;
}

.contact-details {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.contact-detail-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  font-size: 1.1rem;
}

.contact-icon {
  font-size: 1.5rem;
}

.contact-text {
  opacity: 0.95;
}

.contact-form-wrapper {
  background-color: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  padding: 2.5rem;
  border-radius: 16px;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.form-label {
  font-size: 1rem;
  font-weight: 500;
  color: white;
}

.form-input,
.form-textarea {
  padding: 0.875rem;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-family: inherit;
  background-color: rgba(255, 255, 255, 0.2);
  color: white;
  transition: background-color 0.3s;
}

.form-input::placeholder,
.form-textarea::placeholder {
  color: rgba(255, 255, 255, 0.7);
}

.form-input:focus,
.form-textarea:focus {
  outline: none;
  background-color: rgba(255, 255, 255, 0.3);
}

.form-textarea {
  resize: vertical;
  min-height: 120px;
}

.submit-button {
  padding: 1rem 2rem;
  background-color: white;
  color: #8A2BE2;
  border: none;
  border-radius: 8px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
}

.submit-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

@media (max-width: 968px) {
  .contact-content {
    grid-template-columns: 1fr;
  }
  
  .contact-title {
    font-size: 2rem;
  }
}
</style>

