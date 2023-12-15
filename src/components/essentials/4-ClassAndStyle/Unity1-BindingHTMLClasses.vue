<script setup>
import { ref } from 'vue';

  const isActive = ref(true)
  // const hasError = ref(false)

  // const classObject = reactive({
  //   'active': true,
  //   'text-danger': false
  // })

  // Powerful pattern
  // const isActive = ref(true)
  // const error = ref(null)

  // const classObject = computed(() => ({
  //   active: isActive.value && !error.value,
  //   'text-danger': error.value && error.value.type === 'fatal'
  // }))

  // We can also append an array of classes
  // const activeClass = ref('active')
  const errorClass = ref('text-danger')
</script>

<template>
  <!-- <div
    class="static"
    :class="{
      'active': isActive,
      'text-danger': hasError
    }"
  ></div> -->
  <!-- <div :class="classObject"></div> -->
  <!-- <div :class="[activeClass, errorClass]"></div> -->
  <div :class="[{ active: isActive }, errorClass]"></div>
  <!-- If your component has multiple root elements, you would need to define which element will receive this class. 
  You can do this using the $attrs component property: -->
  <div :class="$attrs.class"></div>
  <!-- Now when you pass a class this root element is going to receive the class attributes -->
  <!-- <MyComponent class="baz" /> -->
</template>