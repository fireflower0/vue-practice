<template>
  <div id='home'>
    <HeadLine h1 text='Home' />
    <HeadLine h2 text='Home' />
    <HeadLine h3 text='Home' />
    <HeadLine h4 text='Home' />
    <HeadLine h5 text='Home' />
    <HeadLine h6 text='Home' />

   <FieldSet labelText='TextBox'>
      <TextBox v-model='message1' placeholder='Edit Me' />
      <p>Message is: {{ message1 }}</p>
    </FieldSet>

    <FieldSet labelText='TextArea'>
      <TextArea v-model='message2' placeholder='Edit Me' />
      <p>Message is: {{ message2 }}</p>
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
  },
  data() {
    return {
      message1: 'Hello, Text Box !',
      message2: 'Hello, Text Area !',
    }
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
