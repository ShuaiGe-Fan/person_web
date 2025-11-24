<template>
  <section id="comments" class="comments">
    <div class="comments-container">
      <h2 class="section-title">网站留言</h2>
      <div class="comment-form-container">
        <h3 class="form-title">发表评论</h3>
        <form class="comment-form" @submit.prevent="submitComment">
          <div class="form-row">
            <input
              v-model="form.name"
              type="text"
              placeholder="姓名"
              class="form-input"
              required
            />
            <input
              v-model="form.email"
              type="email"
              placeholder="邮箱"
              class="form-input"
              required
            />
          </div>
          <textarea
            v-model="form.content"
            placeholder="写下你的评论..."
            class="form-textarea"
            rows="5"
            required
          ></textarea>
          <button type="submit" class="submit-btn">发表评论</button>
        </form>
      </div>
      <div class="comments-list">
        <div class="comment-item" v-for="comment in comments" :key="comment.id">
          <div class="comment-avatar">
            <svg width="50" height="50" viewBox="0 0 50 50" fill="none">
              <circle cx="25" cy="25" r="25" fill="#E0E0E0"/>
              <circle cx="25" cy="20" r="8" fill="#9E9E9E"/>
              <path d="M 10 35 Q 25 28 40 35" stroke="#9E9E9E" stroke-width="5" fill="none" stroke-linecap="round"/>
            </svg>
          </div>
          <div class="comment-content">
            <div class="comment-header">
              <span class="comment-name">{{ comment.name }}</span>
              <span class="comment-date">{{ comment.date }}</span>
            </div>
            <p class="comment-text">{{ comment.content }}</p>
            <a href="#" class="reply-link">↩️ 回复</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, reactive } from 'vue'

interface Comment {
  id: number
  name: string
  date: string
  content: string
}

const form = reactive({
  name: '',
  email: '',
  content: ''
})

const comments = ref<Comment[]>([
  {
    id: 1,
    name: '张小明',
    date: '2024-01-20',
    content: '网站设计很棒!界面简洁美观,内容也很有价值。期待更多优质文章!'
  },
  {
    id: 2,
    name: '李小红',
    date: '2024-01-18',
    content: '作为同行,真的很佩服你的技术水平和分享精神。你的文章帮助我解决了很多实际问题。'
  }
])

const submitComment = () => {
  if (form.name && form.email && form.content) {
    const newComment: Comment = {
      id: comments.value.length + 1,
      name: form.name,
      date: new Date().toISOString().split('T')[0],
      content: form.content
    }
    comments.value.unshift(newComment)
    form.name = ''
    form.email = ''
    form.content = ''
  }
}
</script>

<style scoped>
.comments {
  background-color: #ffffff;
  padding: 6rem 2rem;
}

.comments-container {
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

.comment-form-container {
  background-color: #F5F5F5;
  padding: 2rem;
  border-radius: 12px;
  margin-bottom: 3rem;
}

.form-title {
  font-size: 1.5rem;
  color: #333;
  margin: 0 0 1.5rem 0;
  font-weight: 600;
}

.comment-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.form-input,
.form-textarea {
  padding: 0.75rem;
  border: 1px solid #DDD;
  border-radius: 8px;
  font-size: 1rem;
  font-family: inherit;
  transition: border-color 0.3s;
}

.form-input:focus,
.form-textarea:focus {
  outline: none;
  border-color: #8A2BE2;
}

.form-textarea {
  resize: vertical;
  min-height: 120px;
}

.submit-btn {
  padding: 0.875rem 2rem;
  background-color: #8A2BE2;
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 500;
  cursor: pointer;
  transition: background-color 0.3s;
  align-self: center;
}

.submit-btn:hover {
  background-color: #7B1FA2;
}

.comments-list {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.comment-item {
  display: flex;
  gap: 1rem;
  background-color: #F5F5F5;
  padding: 1.5rem;
  border-radius: 12px;
}

.comment-avatar {
  flex-shrink: 0;
}

.comment-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.comment-header {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.comment-name {
  font-weight: 600;
  color: #333;
  font-size: 1rem;
}

.comment-date {
  font-size: 0.85rem;
  color: #999;
}

.comment-text {
  color: #555;
  line-height: 1.6;
  margin: 0;
}

.reply-link {
  color: #8A2BE2;
  text-decoration: none;
  font-size: 0.9rem;
  align-self: flex-start;
  transition: opacity 0.3s;
}

.reply-link:hover {
  opacity: 0.8;
}

@media (max-width: 768px) {
  .form-row {
    grid-template-columns: 1fr;
  }
  
  .section-title {
    font-size: 2rem;
  }
}
</style>

