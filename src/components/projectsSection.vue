<script setup>
import { ref } from 'vue'
import ProjectCard from '@/assets/projectsCard.vue'

// Replace this placeholder data with your real projects
const projects = ref([
  {
    id: 1,
    title: 'Portfolio Site',
    description: 'This site, built with Vue 3, Vite, and Tailwind CSS.',
    tags: ['Vue', 'Tailwind'],
    featured: true,
    links: [
      {
        label: 'GitHub',
        url: 'https://github.com/MahesaKahfi/Portfolio'
      }
    ]
  },
  {
    id: 2,
    title: 'B-Clean',
    description: 'A trash recycling and waste management web app built with React and Laravel.',
    tags: ['React', 'Laravel'],
    featured: false,
    links: [
      {
        label: 'GitHub',
        url: 'https://github.com/MahesaKahfi/B-Clean'
      }
    ]
  },
  {
    id: 3,
    title: 'Anim8',
    description: 'A Web app for anime watchers to view current anime and like their favorite anime built with Vue and Jikan API',
    tags: ['Vue', 'Node.js', 'API'],
    featured: true,
    links: [
      {
        label: 'Client',
        url: 'https://github.com/MahesaKahfi/p2-iproject-client'
      },
      {
        label: 'Server',
        url: 'https://github.com/MahesaKahfi/p2-iproject-server'
      }
    ]
  },
  {
    id: 4,
    title: 'My Portfolio',
    description: 'This portfolio site, built with Vue 3, Vite, and Tailwind CSS.',
    tags: ['Vue', 'Tailwind'],
    featured: true,
    links: [
      {
        label: 'GitHub',
        url: ''
      }
    ]
  },
  {
    id: 5,
    title: 'My Portfolio',
    description: 'This portfolio site, built with Vue 3, Vite, and Tailwind CSS.',
    tags: ['Vue', 'Tailwind'],
    featured: true,
    links: [
      {
        label: 'GitHub',
        url: ''
      }
    ]
  },
  {
    id: 6,
    title: 'My Portfolio',
    description: 'This portfolio site, built with Vue 3, Vite, and Tailwind CSS.',
    tags: ['Vue', 'Tailwind'],
    featured: true,
    links: [
      {
        label: 'GitHub',
        url: ''
      }
    ]
  }
])
</script>

<template>
  <section id="projects" class="px-6 py-20 max-w-5xl mx-auto">
    <h2 class="text-2xl font-semibold text-ink mb-8">Projects</h2>

    <div class="grid gap-5 sm:grid-cols-2 lg:grid-cols-3">
      <ProjectCard
        v-for="project in projects"
        :key="project.id"
        :title="project.title"
        :description="project.description"
        :tags="project.tags"
        :featured="project.featured"
        :links="project.links"
      />
    </div>
  </section>
</template>