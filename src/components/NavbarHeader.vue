<template>
  <nav class="flex flex-col fixed top-0 w-full px-6 py-4 backdrop-blur-md">
    <div class="flex justify-between">
      <button @click="handleMenuToggle">
        <BarsThreeIcon />
      </button>
      <div>Mark Dennis</div>
    </div>
    <div
      class="space-y-4 overflow-hidden transition-all duration-300"
      :class="menuToggle ? 'h-96' : 'h-0'"
    >
      <div class="mt-6">
        <NavbarLinks
          @click="handleMenuToggle"
          v-for="(link, index) in navLinks"
          :key="index"
          :name="link.name"
          :href="link.href"
          :text="link.text"
        />
      </div>
      <hr class="w-full bg-gray-500" />
      <div class="text-xs text-gray-500 space-y-4 text-center">
        <p>
          © 2023 <a class="hover:underline hover:text-gray-50" href="/">Mark Dennis Sanchez</a>. All
          Rights Reserved.
        </p>
        <div class="space-x-2 divide-x-2">
          <a
            @click="handleMenuToggle"
            v-for="(link, index) in socials"
            :key="index"
            target="_blank"
            class="lowercase hover:underline hover:text-gray-50"
            :class="index > 0 && 'pl-2'"
            :href="link.href"
          >
            {{ link.name }}
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import NavbarLinks from './NavbarLinks.vue'
import BarsThreeIcon from './icons/BarsThreeIcon.vue'
import { ref } from 'vue'

const menuToggle = ref(false)

const handleMenuToggle = () => {
  menuToggle.value = !menuToggle.value
}

const navLinks = [
  {
    text: 'Resume',
    name: 'resume',
    href: '/resume'
  },
  {
    text: 'Home',
    name: 'home',
    href: '/'
  },
  {
    text: 'About',
    name: 'about',
    href: '/about'
  },
  {
    text: 'Skills',
    name: 'skills',
    href: '/skills'
  },
  {
    text: 'Projects',
    name: 'projects',
    href: '/projects'
  },
  {
    text: 'Contact',
    name: 'contact',
    href: '/contact'
  }
]

const socials = [
  {
    name: 'facebook',
    href: 'https://facebook.com/sanchez.markdennis'
  },
  {
    name: 'instagram',
    href: 'https://instagram.com/ig.markdennis'
  },
  {
    name: 'linkedin',
    href: 'https://linkedin.com/in/sanchez.markdennis'
  },
  {
    name: 'github',
    href: 'https://github.com/markdennis1'
  }
]
</script>
