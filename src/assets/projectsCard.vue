<script setup>
defineProps({
  title: { type: String, required: true },
  description: { type: String, default: '' },
  tags: { type: Array, default: () => [] },
  featured: { type: Boolean, default: false },
  links: { type: Array, default: () => [] }
})
</script>

<template>
  <article class="border border-muted/30 rounded-lg p-5 bg-white hover:border-primary transition-colors">
    <h3 class="font-medium text-ink mb-1">{{ title }}</h3>
    <p class="text-sm text-ink/70 mb-3">{{ description }}</p>

    <ul v-if="tags.length" class="flex flex-wrap gap-2 mb-3">
      <li
        v-for="tag in tags"
        :key="tag"
        class="text-xs px-2 py-0.5 rounded-full border border-muted/30 text-ink/70"
      >
        {{ tag }}
      </li>
    </ul>

    <div class="flex items-center justify-between">
      <span v-if="featured" class="text-xs text-primary">featured</span>
      <div class="flex gap-3 ml-auto">
        <a 
          v-for="item in links" 
          :key="item.label" 
          :href="item.url" 
          target="_blank" 
          rel="noopener" 
          class="text-sm text-accent hover:underline">
          {{ item.label }} ↗
        </a>
      </div>
    </div>
  </article>
</template>