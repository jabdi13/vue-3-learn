<script setup>
import Unity1DeclaringReactiveState from './components/essentials/2-ReactivityFundamentals/composition-api/Unity1-DeclaringReactiveState.vue';

</script>

<template>
  <Unity1DeclaringReactiveState></Unity1DeclaringReactiveState>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
