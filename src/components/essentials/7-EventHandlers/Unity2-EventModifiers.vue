<script setup>
function onSubmit() {
  console.log("Prevented")
}
function submit() {
  console.log("Key pressed")
}
</script>

<template>
  <form @submit.prevent="onSubmit">
    <!-- only call `submit` when the `key` is `Enter` -->
    <input @keyup.enter="submit" />
  </form>
</template>