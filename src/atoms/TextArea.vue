<template>
  <textarea
    class='text'
    :value='value'
    :placeholder='placeholder'
  />
</template>

<script>
export default {
  name: 'TextArea',
  props: {
    value: String,
    placeholder: String
  }
}
</script>

<style scoped>
.text {
  padding: 5px;
  border-radius: 3px;
  border: 1px solid #212121;
  font-size: 14px;
}
</style>
