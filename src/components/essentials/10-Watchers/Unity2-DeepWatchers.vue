<script setup>
import { reactive, watch } from 'vue'
const obj = reactive({ count: 0 })
const state = reactive({ someObject: {} })

watch(obj, (newValue, oldValue) => {
  // fires on nested property mutations
  // Note: `newValue` will be equal to `oldValue` here
  // because they both point to the same object!
})

watch(
  () => state.someObject,
  () => {
    // fires only when state.someObject is replaced
  }
)

watch(
  () => state.someObject,
  (newValue, oldValue) => {
    // Note: `newValue` will be equal to `oldValue` here
    // *unless* state.someObject has been replaced
  },
  { deep: true }
)

obj.count++
</script>