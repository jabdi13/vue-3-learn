<!-- <script>
  import { ref } from 'vue'

  export default {
    setup() {
      const count = ref(0);

      function increment() {
        count.value++
      }

      return {
        count,
        increment
      }
    }
  }

</script> -->

<script setup>
  import { ref } from 'vue'

  const count = ref(0)

  function increment() {
    count.value++
  }
</script>

<template>
  <div>{{ count }}</div>
  <button @click="increment">++</button>
</template>

