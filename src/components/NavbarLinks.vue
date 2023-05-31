<template>
  <RouterLink
    :class="`block w-full py-2 font-thin text-center hover:text-white 
    ${route.name === props.name ? 'text-white' : 'text-gray-500'}`"
    :to="props.href"
  >
    {{ props.text }}
  </RouterLink>
</template>

<script setup lang="ts">
import { RouterLink, useRoute } from 'vue-router'

const route = useRoute()

const props = defineProps({
  name: {
    type: String,
    required: true
  },
  href: {
    type: String,
    required: true
  },
  text: {
    type: String,
    required: true
  }
})
</script>
