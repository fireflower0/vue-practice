<template>
  <input
    class='date'
    type='date'
    @input='setDate'
  />
</template>

<script>
export default {
  name: 'Date',
  props: {
    date: String
  },
  methods: {
    setDate (e) { this.$emit('input', e.target.value) }
  }
}
</script>

<style scoped>
.date {
  margin: 5px;
  padding: 0 10px;
  height: 30px;
  border: 1px solid #263238;
  border-radius: 5px;
  background-color: #ECEFF1;
  font-size: 14px;
}
</style>
