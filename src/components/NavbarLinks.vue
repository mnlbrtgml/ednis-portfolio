<template>
  <a
    class="nav-link flex w-full py-2 gap-2 font-thin justify-center transition-all text-gray-500 hover:text-white hover:pl-4"
    :href="props.href"
  >
    {{ props.name }}
  </a>
</template>

<script setup lang="ts">
const props = defineProps({
  name: {
    type: String,
    required: true
  },
  href: {
    type: String,
    required: true
  }
})
</script>
