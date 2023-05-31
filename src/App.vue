<template>
    <header>
      <NavbarHeader />
    </header>
    <main class="px-6 mt-14">
      <RouterView />
    </main>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavbarHeader from './components/NavbarHeader.vue'
</script>
