<template>
  <input
    class='range'
    type='range'
    @input='setRange'
  />
</template>

<script>
export default {
  name: 'Range',
  methods: {
    setRange (e) { this.$emit('input', e.target.value) }
  }
}
</script>

<style scoped>
.range {
  margin: 5px;
}
</style>
