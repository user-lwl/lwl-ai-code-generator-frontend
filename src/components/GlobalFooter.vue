<template>
  <a-layout-footer class="footer">
    <div class="footer-content">
      <p class="copyright">
        Lwl Ai Code Generator©2026 by
        <a
          href="https://www.user-lwl.cn"
          target="_blank"
          rel="noopener noreferrer"
          class="author-link"
        >
          user-lwl
        </a> | <a href="https://beian.miit.gov.cn/" target="_blank" rel="noopener noreferrer">鲁ICP备2024080109号-3</a>
      </p>
    </div>
  </a-layout-footer>
</template>

<script setup lang="ts">
// 无需额外的响应式数据
</script>

<style scoped>
.footer {
  background: rgba(255, 255, 255, 0.8);
  backdrop-filter: blur(10px);
  text-align: center;
  padding: 20px;
  border-top: 1px solid rgba(102, 126, 234, 0.1);
}

.copyright {
  margin: 0;
  color: #666;
  font-size: 14px;
}
</style>
