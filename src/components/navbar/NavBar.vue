<script setup lang="ts">
import Button from '@/components/button/Button.vue';
import IconLogo from '@/components/icons/IconLogo.vue';
import IconMenu from '@/components/icons/IconMenu.vue';
import NavBtns from '@/components/navbar/NavBtns.vue';
import NavLinks from '@/components/navbar/NavLinks.vue';
import NavMobMenu from '@/components/navbar/NavMobMenu.vue';
import { ref } from 'vue';

const isMenuOpen = ref(false)
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <div class="header">
    <div class="header-links">
      <IconLogo />
      <NavLinks class="desk-nav" />
    </div>
    <NavBtns class="desk-nav"/>
    <Button class="icon header-menu-btn" @clicked="toggleMenu">
      <template #startIcon>
        <IconMenu />
      </template>
    </Button>
  </div>
  <NavMobMenu v-if="isMenuOpen" @close="toggleMenu" />
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
  margin: 1rem 0 0;
  height: 68px;
  flex: auto;
}
.header-links {
  display: flex;
  gap: 96px;
}

.header-menu-btn {
  display: none;
}

@media (max-width: 768px) {
  .header {
    padding: 0 2rem;
    gap: 1rem;
  }
  .desk-nav {
    display: none;
  }
  .header-menu-btn {
    display: flex;
  }
}
</style>