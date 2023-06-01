<template>
  <header>
    <NavbarHeader />
  </header>
  <main class="px-6 mt-14">
    <HomeView />
    <hr />
    <AboutView />
    <hr />
    <SkillsView />
    <hr />
    <ProjectsView />
    <hr />
    <ResumeView />
    <hr />
    <ContactView />
  </main>
</template>

<script setup lang="ts">
import NavbarHeader from './components/NavbarHeader.vue'
import HomeView from '@/views/HomeView.vue'
import AboutView from '@/views/AboutView.vue'
import SkillsView from '@/views/SkillsView.vue'
import ProjectsView from '@/views/ProjectsView.vue'
import ResumeView from '@/views/ResumeView.vue'
import ContactView from '@/views/ContactView.vue'

window.addEventListener('scroll', () => {
  let current = ''

  const sections = document.querySelectorAll('section')

  sections.forEach((section) => {
    const sectionTop = section.offsetTop
    if (scrollY + 80 >= sectionTop) {
      current = section.getAttribute('id') || ''
    }
  })

  const navLinks: NodeListOf<HTMLAnchorElement> = document.querySelectorAll('.nav-link')
  navLinks.forEach((li) => {
    li.classList.remove('text-white')
    if (li.href.includes(current)) {
      li.classList.add('text-white')
    }
  })
})
</script>
