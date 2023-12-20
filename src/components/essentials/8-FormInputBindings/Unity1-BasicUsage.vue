<script setup>
import { ref } from 'vue';

const text = ref('')
const message = ref('')
const checkedCheckbox = ref(true)
const checkedNames = ref([])
const picked = ref('')
const selected = ref('A')
const selected1 = ref('A')

const options = ref([
  { text: 'One', value: 'A' },
  { text: 'Two', value: 'B' },
  { text: 'Three', value: 'C' }
])
const first = 'first'
const second = 'second'
const pick = ref('')
</script>

<template>
  <input type="text" v-model="text">
  <p>Message is: {{ text }}</p>
  <span>Multiline message is:</span>
  <p style="white-space: pre-line;">{{ message }}</p>
  <textarea v-model="message" placeholder="add multiple lines"></textarea>
  <div>
    <input type="checkbox" id="checkbox" v-model="checkedCheckbox">
    <label for="checkbox">{{ checkedCheckbox }}</label>
  </div>
  <div>Checked names: {{ checkedNames }}</div>

  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
  <label for="jack">Jack</label>

  <input type="checkbox" id="john" value="John" v-model="checkedNames">
  <label for="john">John</label>

  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
  <label for="mike">Mike</label>
  <div>Picked: {{ picked }}</div>

  <input type="radio" id="one" value="One" v-model="picked" />
  <label for="one">One</label>

  <input type="radio" id="two" value="Two" v-model="picked" />
  <label for="two">Two</label>
  <div>
    <div>Selected: {{ selected }}</div>

    <select v-model="selected">
      <option disabled value="">Please select one</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </div>
  <div>
    <select v-model="selected">
      <option v-for="option in options" :value="option.value" :key="option.text">
        {{ option.text }}
      </option>
    </select>

    <div>Selected: {{ selected }}</div>
  </div>
  <div>
    <input type="radio" v-model="pick" :value="first" />
    <input type="radio" v-model="pick" :value="second" />
    <p>picked {{ pick }}</p>
  </div>
  <div>
    <select v-model="selected1">
      <!-- inline object literal -->
      <option :value="{ number: 123 }">123</option>
    </select>
  </div>
</template>