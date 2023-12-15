<script setup>
import { ref } from 'vue'
const items = ref([{ message: 'Foo' }, { message: 'Bar' }])
</script>

<template>
  <!-- You can destructure object item -->
  <li v-for="(item, index) in items" :key="index">
    {{ item.message }}
  </li>
</template>