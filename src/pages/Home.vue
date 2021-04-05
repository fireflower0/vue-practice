<template>
  <div id='home'>
    <h1>Home</h1>
    <TextBox value='Hello, world!' />
  </div>
</template>

<script>
import TextBox from '../atoms/TextBox.vue'

export default {
  components: {
    TextBox
  }
}
</script>

<style>
#home {
  margin: 5px;
  padding: 10px;
  background-color: #FFF3E0;
}
</style>
