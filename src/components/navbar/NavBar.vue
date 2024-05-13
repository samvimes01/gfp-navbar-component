<script setup lang="ts">
import Button from '@/components/button/Button.vue';
</script>

<template>
  <div class="header">
    <div class="header-links">
      <img src="/abstractly.png" alt="Company logo" class="logo" />
      <nav class="navigation">
        <a href="#" class="nav-link">Home</a>
        <a href="#" class="nav-link">Features</a>
        <a href="#" class="nav-link">Pricing</a>
        <a href="#" class="nav-link">About us</a>
        <a href="#" class="nav-link disabled">Contact</a>
      </nav>
    </div>
    <div class="header-buttons">
      <Button class="secondary">Learn more</Button>
      <Button class="primary">See pricing</Button>
    </div>
  </div>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 96px;
  max-width: 1216px;
  font-size: 1rem;
  font-weight: var(--font-medium);
  line-height: 1.5rem;
  padding: 0.875rem 0;
  height: 68px;
  flex: auto;
}
.header-links {
  display: flex;
  gap: 96px;
}
.header-buttons {
  display: flex;
  gap: 16px;
}
@media (max-width: 991px) {
  .header {
    padding: 0 20px;
  }
}

.logo {
  width: 112px;
  max-width: 100%;
  margin: auto 0;
}

.navigation {
  display: flex;
  gap: 32px;
  color: var(--color-text);
  justify-content: space-between;
  flex: 1;
  margin: auto 0;
}

@media (max-width: 991px) {
  .navigation {
    flex-wrap: wrap;
  }
}

.nav-link {
  text-decoration: none;
  color: inherit;
}
.nav-link:hover, .nav-link:focus {
  color: var(--color-neutral-900)
}
.nav-link:focus {
  box-shadow: 0 0 0 4px rgba(68, 76, 231, 0.12);
  background: #fff;
}
.nav-link.disabled {
  color: var(--color-neutral-400);
  pointer-events: none;
}


</style>