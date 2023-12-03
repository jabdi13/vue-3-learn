<script setup>

  const msg = "Hello vue"
  const rawHtml = '<span style="color: red">This should be red.</span>'
  const id = "newId"
  const isButtonDisabled = true
  const objectOfAttrs = {
      id: 'container',
      class: 'wrapper'
    }
</script>

<template>
  <!-- Text interpolation -->
  <span>Message: {{ msg }}</span>
  <!-- Raw HTML -->
  <p>Using text interpolation: {{ rawHtml }}</p>
  <p>Using v-html directive: <span v-html="rawHtml"></span></p>
  
  <!-- Attribute Bindings -->
  <div v-bind:id="id">New ID</div>
  <!-- Shorthand binding -->
  <div :id="'idInterpolated'">Shorthand binding</div>
  <!-- Boolean Attributes -->
  <button :disabled="isButtonDisabled">Button</button>
  <!-- Dynamically Binding Multiple Attributes -->
  <div v-bind="objectOfAttrs">objectOfAttrs</div>
</template>