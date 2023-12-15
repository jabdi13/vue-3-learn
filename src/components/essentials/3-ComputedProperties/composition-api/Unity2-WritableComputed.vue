<script setup>
import { computed, ref } from 'vue';

  const firstName = ref('Abdiel')
  const lastName = ref('Ortega')

  const fullName = computed({
    get() {
      return `${firstName.value} ${lastName.value}`
    },
    set(newValue) {
      [firstName.value, lastName.value] = newValue.split(' ')
    }
  })
</script>