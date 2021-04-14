<template>
  <input
    class='color'
    type='color'
    @input='setColor'
  />
</template>

<script>
export default {
  name: 'Color',
  methods: {
    setColor (e) { this.$emit('input', e.target.value) }
  }
}
</script>

<style scoped>
.color {
  margin: 5px;
}
</style>
