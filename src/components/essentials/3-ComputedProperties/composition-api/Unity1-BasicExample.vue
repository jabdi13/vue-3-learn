<script setup>
import { computed, reactive } from 'vue';

  const author = reactive({
    name: 'John Doe',
    books: [
      'Vue 2 - Advanced Guide',
      'Vue 3 - Basic Guide',
      'Vue 4 - The Mystery'
    ]
  })
  const publishedBookMessage = computed(() => {
    return author.books.length > 0 ? 'Yes' : 'No'
  })
</script>

<template>
  <p>Has published books:</p>
  <span>{{ publishedBookMessage }}</span>
</template>