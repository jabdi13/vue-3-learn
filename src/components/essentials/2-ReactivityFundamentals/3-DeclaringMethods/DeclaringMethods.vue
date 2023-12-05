<script>
export default {
  data() {
    return {
      count: 0
    }
  },
  methods: {
    // Remember do not declare arrow functions
    increment() {
      this.count++
    }
  },
  mounted() {
    // methods can be called in lifecycle hooks, or other methods!
    this.increment()
  }
}
</script>

<template>
  <button @click="increment">{{ count }}</button>
</template>