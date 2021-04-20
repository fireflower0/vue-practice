<template>
  <button class='button' @click='handleClick' >
    {{ labelText }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    labelText: String,
    handleClick: Function
  }
}
</script>

<style scoped>
.button {
  padding: 5px;
  margin-left: 5px;
  width: 100px;
  background-color: #90A4AE;
  border: none;
  border-radius: 3px;
}
</style>
