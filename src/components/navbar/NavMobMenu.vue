<script setup lang="ts">
import Button from '@/components/button/Button.vue';
import IconClose from '@/components/icons/IconClose.vue';
import IconLogo from '@/components/icons/IconLogo.vue';
import NavBtns from '@/components/navbar/NavBtns.vue';
import NavLinks from '@/components/navbar/NavLinks.vue';

defineEmits(['close'])
</script>

<template>
  <div class="overlay">
    <div class="menu">
      <div class="items">
        <div class="header">
          <IconLogo />
          <Button class="icon header-menu-btn" @clicked="$emit('close')">
            <template #startIcon>
              <IconClose />
            </template>
          </Button>
        </div>
        <NavLinks />
      </div>
      <NavBtns />
    </div>
  </div>
</template>

<style scoped>
.overlay {
  position: absolute;
  width: 100%;
  height: 100vh;
  background: #0a0a0ab3;
  z-index: 1;
}
.menu {
  height: 100%;
  width: 95%;
  overflow-y: auto;
  background: #fff;
  padding: 2rem 1rem 1rem;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  justify-content: space-between;
}

.header {
  display: flex;
  justify-content: space-between;
}

.items {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}
</style>
