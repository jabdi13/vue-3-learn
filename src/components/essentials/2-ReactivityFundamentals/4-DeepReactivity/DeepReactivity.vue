<script>
export default {
  data() {
    // In Vue, state is deeply reactive by default. This means you can expect changes to be detected even when you mutate nested objects or arrays
    return {
      obj: {
        nested: { count: 0 },
        arr: ['foo', 'bar']
      }
    }
  },
  methods: {
    mutateDeeply() {
      // these will work as expected.
      this.obj.nested.count++
      this.obj.arr.push('baz')
    }
  }
}
</script>