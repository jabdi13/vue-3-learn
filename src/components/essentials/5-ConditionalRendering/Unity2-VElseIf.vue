<script setup>
import { ref } from 'vue';

  const showLetter = ref('C')
</script>

<template>
  <div v-if="showLetter === 'A'">
    A
  </div>
  <div v-else-if="showLetter === 'B'">
    B
  </div>
  <div v-else-if="showLetter === 'C'">
    C
  </div>
  <div v-else>
    Not A/B/C
  </div>

  <h1 v-show="showLetter === 'A'">Hello!</h1>
</template>