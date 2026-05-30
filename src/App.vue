<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="app-shell">
    <header class="site-header">
      <RouterLink class="brand" to="/">
        <img alt="" class="brand-mark" src="@/assets/logo.svg" width="32" height="32" />
        <span>AI Work</span>
      </RouterLink>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </header>

    <RouterView />
  </div>
</template>

<style scoped>
.app-shell {
  min-height: 100vh;
}

.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1.5rem;
  padding: 1.25rem 0;
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: 0.65rem;
  color: var(--color-heading);
  font-size: 1rem;
  font-weight: 700;
}

.brand:hover {
  background: transparent;
}

.brand-mark {
  display: block;
}

nav {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  font-size: 0.95rem;
}

nav a.router-link-exact-active {
  color: var(--color-heading);
  border-color: var(--color-border-hover);
  background: var(--color-background-soft);
}

nav a.router-link-exact-active:hover {
  background: var(--color-background-soft);
}

nav a {
  display: inline-block;
  border: 1px solid transparent;
  border-radius: 8px;
  padding: 0.4rem 0.75rem;
  color: var(--color-text);
}

@media (max-width: 560px) {
  .site-header {
    align-items: flex-start;
    flex-direction: column;
  }
}
</style>
