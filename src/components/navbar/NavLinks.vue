<template>
  <nav class="navigation">
    <a href="#" class="nav-link">Home</a>
    <a href="#" class="nav-link">Features</a>
    <a href="#" class="nav-link">Pricing</a>
    <a href="#" class="nav-link">About us</a>
    <a href="#" class="nav-link">Contact</a>
  </nav>
</template>

<style scoped>
.navigation {
  display: flex;
  gap: 2rem;
  color: var(--color-text);
  justify-content: space-between;
  flex: 1;
  margin: auto 0;
}

.nav-link {
  text-decoration: none;
  color: inherit;
  padding: 0 2px;
}
.nav-link:hover,
.nav-link:focus {
  color: var(--color-neutral-900);
}
.nav-link:focus {
  box-shadow: 0 0 0 4px rgba(68, 76, 231, 0.12);
  background: #fff;
}
.nav-link.disabled {
  color: var(--color-neutral-400);
  pointer-events: none;
}

@media (max-width: 768px) {
  .navigation {
    flex-direction: column;
    gap: 0.5rem;
  }
  .nav-link {
    padding: 0.5rem 0.75rem;
    height: 2.25rem;
  }
}
</style>
