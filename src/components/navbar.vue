<script setup>
const links = [
  { label: 'Home', href: '#home' },
  { label: 'Projects', href: '#projects' },
  { label: 'About', href: '#about' },
  { label: 'Contact', href: '#contact' }
]
</script>

<template>
  <header class="sticky top-0 z-10 flex items-center justify-between px-6 py-4 bg-paper/90 backdrop-blur border-b border-muted/20">
    <a href="#" class="text-lg font-bold">Mahesa Kahfi</a>
    
    <nav class="hidden sm:flex gap-6">
      <a
        v-for="link in links"
        :key="link.href"
        :href="link.href"
        class="text-sm text-ink/80 hover:text-primary transition-colors"
      >
        {{ link.label }}
      </a>
    </nav>

    <a
      href="/resume.pdf"
      download
      class="text-sm px-4 py-2 rounded-md bg-primary text-paper hover:opacity-90 transition-opacity"
    >
      My Resume
    </a>

    
  </header>
</template>