<template>
  <footer class="footer">
    <div class="footer-container">
      <p class="footer-text">
        © 2024 飞飞公主的个人简历网站 | 
        <a href="https://beian.miit.gov.cn/" target="_blank" class="footer-link">
          晋ICP备2025069505号
        </a>
      </p>
    </div>
  </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer {
  background-color: #333;
  padding: 2rem;
  border-top: 2px solid #8A2BE2;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.footer-text {
  color: #fff;
  font-size: 0.9rem;
  margin: 0;
}

.footer-link {
  color: #BA55D3;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-link:hover {
  color: #DA70D6;
}
</style>

