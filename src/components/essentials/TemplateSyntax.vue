<script setup>
import { ref } from 'vue';

  const msg = ref("Hello vue")
</script>

<template>
  <!-- Text interpolation -->
  <span>Message: {{ msg }}</span>
</template>