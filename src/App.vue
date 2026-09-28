<script setup>
import navbar from './components/navbar.vue'
import homeSection from './components/homeSection.vue'
import projectsSection from './components/projectsSection.vue'

const specialties = ['Vue', 'React', 'Laravel', 'JavaScript', 'Node.js', 'Tailwind CSS']
</script>

<template>
  <navbar />
  <main>
    <homeSection />
    <projectsSection />
 
    <section id="about" class="min-h-[50vh] flex items-center justify-center text-ink/40 border-t border-muted/10">
      About section — coming next
    </section>
 
    <section id="contact" class="min-h-[50vh] flex items-center justify-center text-ink/40 border-t border-muted/10">
      Contact section — coming next
    </section> 
  </main>
</template>

<style scoped></style>
