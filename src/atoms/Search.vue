<template>
  <input
    class='search'
    type='search'
    @input='setValue'
  />
</template>

<script>
export default {
  name: 'Search',
  methods: {
    setValue (e) { this.$emit('input', e.target.value) }
  }
}
</script>

<style scoped>
.search {
  margin: 5px;
  padding: 5px;
  border-radius: 3px;
  border: 1px solid #212121;
  font-size: 14px;
}
</style>
