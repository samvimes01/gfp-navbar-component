<script setup lang="ts">
import Button from '@/components/button/Button.vue';
</script>

<template>
  <div class="header-buttons">
    <Button class="secondary">Learn more</Button>
    <Button class="primary">See pricing</Button>
  </div>
</template>

<style scoped>
.header-buttons {
  display: flex;
  gap: 16px;
}
@media (max-width: 768px) {
  .header-buttons {
    flex-direction: column;
  }
}
</style>
