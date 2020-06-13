<script>
export default {
  props: ['brand', 'copyrightYear', 'navLinks']
}
</script>

<template>
  <footer class="footer">
    <ul class="footer-nav-list">
      <li v-for="link in navLinks" :key="link.label">
        <a class="footer-nav-link" href="#">{{ link.label }}</a>
      </li>
    </ul>
    {{ brand }} © {{ copyrightYear }}
  </footer>
</template>

<style scoped>
.footer {
  margin-top: 2rem;
  padding-top: 1rem;
  padding-bottom: 2rem;
  border-top: 2px solid #ccc;
}

.footer-nav-list {
  display: flex;
  justify-content: center;
}

.footer-nav-list {
  list-style: none;
}

.footer-nav-link {
  text-decoration: none;
  padding-right: 1rem;
}
</style>
