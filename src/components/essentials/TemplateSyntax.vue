<script setup>

  const msg = "Hello vue"
  const rawHtml = '<span style="color: red">This should be red.</span>'
  const id = "newId"
  const isButtonDisabled = true
  const objectOfAttrs = {
      id: 'container',
      class: 'wrapper'
  }
  const doSomething = () => console.log("Click")
  const attributeName = "href"
  const url = "https://vuejs.org/guide/essentials/template-syntax.html"
  const eventName = "click"
  const onSubmit = () => console.log("Click")
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

  <!-- Directive v-on -->
  <a v-on:click="doSomething"> ... </a>
  <!-- shorthand -->
  <a @click="doSomething"> ... </a>

  <!-- Dynamic Arguments -->
  <!--
  Note that there are some constraints to the argument expression,
  as explained in the "Dynamic Argument Value Constraints" and "Dynamic Argument Syntax Constraints" sections below.
  -->
  <a v-bind:[attributeName]="url"> ... </a>

  <!-- shorthand -->
  <a :[attributeName]="url"> ... </a>
  <a v-on:[eventName]="doSomething"> ... </a>

  <!-- shorthand -->
  <a @[eventName]="doSomething"> ... </a>
  
  <!-- Modifiers -->
  <form @submit.prevent="onSubmit">...</form>
</template>