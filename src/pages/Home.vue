<template>
  <div id='home'>
    <HeadLine h1 text='Home' />
    <HeadLine h2 text='Home' />
    <HeadLine h3 text='Home' />
    <HeadLine h4 text='Home' />
    <HeadLine h5 text='Home' />
    <HeadLine h6 text='Home' />

    <FieldSet labelText='TextBox'>
      <TextBox value='Hello, world!' />
    </FieldSet>

    <FieldSet labelText='TextArea'>
      <TextArea placeholder='Sample' value='Hello, world!' />
    </FieldSet>
  </div>
</template>

<script>
import HeadLine from '../atoms/HeadLine.vue'
import FieldSet from '../atoms/FieldSet.vue'
import TextBox from '../atoms/TextBox.vue'
import TextArea from '../atoms/TextArea.vue'

export default {
  components: {
    HeadLine,
    TextBox,
    TextArea,
    FieldSet
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
