<template>
  <audio class='audio' controls src='src' />
</template>

<script>
export default {
  name: 'Audio',
  props: {
    src: String
  }
}
</script>

<style scoped>
.audio {
  margin: 5px;
}
</style>
