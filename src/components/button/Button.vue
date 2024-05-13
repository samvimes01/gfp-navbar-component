<script setup lang="ts">
defineEmits(['clicked'])
</script>

<template>
  <button type="button" class="button" @click="$emit('clicked')">
    <span class="label"><slot></slot></span>
  </button>
</template>

<style scoped>
.button {
  display: flex;
  justify-content: center;
  gap: 6px;
  padding: 10px 16px;
  border-radius: 4px;
  box-shadow:
    0px 1px 3px 0px rgba(0, 0, 0, 0.1),
    0px 1px 2px 0px rgba(0, 0, 0, 0.06);
  cursor: pointer;
  height: 44px;
}
.button:disabled {
  background: #f5f5f5;
  color: var(--color-neutral-400);
  cursor: not-allowed;
  border: none;
  box-shadow: none;
}

.label {
  padding: 0px 2px;
  font-weight: var(--font-medium);
  font-size: 1rem;
  line-height: 1.5rem;
}


.secondary {
  border: 1px solid #e5e5e5;
  background-color: #fff;
  color: var(--color-neutral-900);
}
.secondry:hover:not(:disabled) {
  box-shadow:
    0 1px 2px 0 rgba(0, 0, 0, 0.06),
    0 1px 3px 0 rgba(0, 0, 0, 0.1);
  background: #fafafa;
}
.secondry:focus:not(:disabled) {
  box-shadow: 0 0 0 4px rgba(68, 76, 231, 0.12);
  background: #fafafa;
}

.primary {
  background-color: var(--color-indigo-700);
  color: #fff;
  border: none;
}
.primary:hover:not(:disabled) {
  box-shadow:
    0 1px 2px 0 rgba(0, 0, 0, 0.06),
    0 1px 3px 0 rgba(0, 0, 0, 0.1);
  background: var(--color-indigo-800);
}
.primary:focus:not(:disabled) {
  box-shadow: 0 0 0 4px rgba(68, 76, 231, 0.12);
  background: var(--color-indigo-800);
}
</style>
