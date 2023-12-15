<script setup>
import { reactive } from 'vue';

  const state = reactive({ count: 0 })
</script>

<template>
  <div>
    <button @click="state.count++">
      {{ state.count }}
    </button>
  </div>
</template>