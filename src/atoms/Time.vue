<template>
  <input
    class='time'
    type='time'
    @input='setTime'
  />
</template>

<script>
export default {
  name: 'Time',
  props: {
    time: String
  },
  methods: {
    setTime (e) { this.$emit('input', e.target.value) }
  }
}
</script>

<style scoped>
.time {
  margin: 5px;
  padding: 0 10px;
  height: 30px;
  border: 1px solid #263238;
  border-radius: 5px;
  background-color: #ECEFF1;
  font-size: 14px;
}
</style>
