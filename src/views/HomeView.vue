<template>
  <section id="home" class="min-h-screen">
    <dotlottie-player
      autoplay
      loop="true"
      mode="normal"
      src="https://assets10.lottiefiles.com/packages/lf20_l3sfdi9x.json"
      style="width: 100%"
    >
    </dotlottie-player>
    <div class="space-y-6">
      <div>
        <p class="text-gray-500 font-bold">Software Developer</p>
        <h2 class="text-2xl">Mark Dennis Sanchez</h2>
      </div>
      <p class="text-gray-500">
        Committed to delivering innovative web solutions, I am eager to empower dynamic
        organizations as a versatile Full Stack Developer.
      </p>
      <ButtonDefault class="w-1/2">Resume</ButtonDefault>
    </div>
  </section>
</template>
<script setup lang="ts">
import { ButtonDefault } from '@/components'
</script>
