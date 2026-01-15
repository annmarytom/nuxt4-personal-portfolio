<template>
  <div>
    <Header />
    <!-- Page content will appear here -->
    <main>
      <slot />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Footer from "~/components/Footer.vue";
import Header from "~/components/Header.vue";
</script>
