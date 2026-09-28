<script setup>
const specialties = ['Vue', 'React', 'Laravel', 'Java', 'JavaScript', 'Node.js', 'Tailwind CSS']
</script>

<template>
  <section id="home" class="min-h-[80vh] flex flex-col items-center justify-center text-center px-6 py-20">
    <h1 class="text-3xl sm:text-4xl font-semibold text-ink mb-2">
      Mahesa Kahfi "Mika"
    </h1>

    <p class="text-lg text-primary font-medium mb-4">
      Web developer based in Indonesia
    </p>

    <p class="max-w-md text-ink/70 mb-6">
      Passionate web developer with a focus on creating engaging and user-friendly web applications. 
      Skilled in modern web technologies and always eager to learn and adapt to new challenges.
    </p>

    <ul class="flex flex-wrap justify-center gap-2 mb-8">
      <li
        v-for="skill in specialties"
        :key="skill"
        class="text-xs px-3 py-1 rounded-full border border-muted/30 text-ink/70"
      >
        {{ skill }}
      </li>
    </ul>

    <div class="flex gap-4">
      <a
        href="#projects"
        class="text-sm px-5 py-2.5 rounded-md bg-primary text-paper hover:opacity-90 transition-opacity"
      >
        View Projects
      </a>
      <a
        href="https://github.com/MahesaKahfi"
        target="_blank"
        rel="noopener"
        class="text-sm px-5 py-2.5 rounded-md border border-accent text-accent hover:bg-accent hover:text-paper transition-colors"
      >
        GitHub ↗
      </a>
    </div>
  </section>
</template>