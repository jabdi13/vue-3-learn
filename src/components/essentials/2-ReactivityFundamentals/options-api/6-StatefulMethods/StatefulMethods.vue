<script>
import { debounce } from 'lodash-es'
/**
 * However, this approach is problematic for components that are reused because a debounced function is stateful: it maintains 
 * some internal state on the elapsed time. If multiple component instances share the same debounced function, they will interfere 
 * with one another.
 */
// export default {
//   methods: {
//     // Debouncing with Lodash
//     click: debounce(function () {
//       // ... respond to click ...
//     }, 500)
//   }
// }
/**
 * To keep each component instance's debounced function independent of the others, we can create the debounced version 
 * in the created lifecycle hook
 */
export default {
  created() {
    // each instance now has its own copy of debounced handler
    this.debouncedClick = debounce(this.click, 500)
  },
  unmounted() {
    // also a good idea to cancel the timer
    // when the component is removed
    this.debouncedClick.cancel()
  },
  methods: {
    click() {
      // ... respond to click ...
    }
  }
}
</script>