<template>
  <div class="app">
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
<script setup>
  definePageMeta({
  layoutTransition: {
    name: 'layout-fade'
  }
})
</script>
<style>
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.layout-fade-enter-active,
.layout-fade-leave-active {
  transition: opacity 0.5s;
}

.layout-fade-enter-from,
.layout-fade-leave-to {
  opacity: 0;
}
</style>
