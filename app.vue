<template>
  <div>
    <Navbar />          <!-- Global navigation -->
    <NuxtLayout>        <!-- Enables per-page layout support -->
      <NuxtPage />      <!-- Renders the actual page -->
    </NuxtLayout>
    <NuxtRouteAnnouncer />
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'; // Explicit import is safer
</script>
