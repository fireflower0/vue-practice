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

    <FieldSet labelText='Radio'>
      <Radio
        v-model='selectedValue'
        :options='options'
        :defaultValue='selectedValue'
      />
      <p>Selected item is: {{ selectedValue }}</p>
    </FieldSet>
  </div>
</template>

<script>
import HeadLine from '../atoms/HeadLine.vue'
import FieldSet from '../atoms/FieldSet.vue'
import TextBox from '../atoms/TextBox.vue'
import TextArea from '../atoms/TextArea.vue'
import Radio from '../atoms/Radio.vue'

export default {
  components: {
    HeadLine,
    TextBox,
    TextArea,
    FieldSet,
    Radio
  },
  data() {
    return {
      message1: 'Hello, Text Box !',
      message2: 'Hello, Text Area !',
      selectedValue: 'Orange',
      options: [
        { id: 0, groupName: 'fruits', value: 'Apple' },
        { id: 1, groupName: 'fruits', value: 'Orange' },
        { id: 2, groupName: 'fruits', value: 'Grape' },
      ]
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
