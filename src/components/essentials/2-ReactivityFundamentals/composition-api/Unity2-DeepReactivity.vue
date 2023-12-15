<script setup>
  import { ref } from 'vue'

  const obj = ref({
    nested: {},
    arr: ['foo', 'bar']
  })

  function mutateDeeply() {
    // these will work as expected.
    obj.value.nested.count++
    obj.value.arr.push('baz')
  }
</script>