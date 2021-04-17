<template>
  <input
    class='number'
    type='number'
    @input='setValue'
  />
</template>

<script>
export default {
  name: 'Number',
  methods: {
    setValue (e) { this.$emit('input', e.target.value) }
  }
}
</script>

<style scoped>
.number {
  margin: 5px;
  padding: 5px;
  border-radius: 3px;
  border: 1px solid #212121;
  font-size: 14px;
}
</style>
