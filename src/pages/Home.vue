<template>
  <div id='home'>
    <HeadLine h1 text='Home' />
    <HeadLine h2 text='Home' />
    <HeadLine h3 text='Home' />
    <HeadLine h4 text='Home' />
    <HeadLine h5 text='Home' />
    <HeadLine h6 text='Home' />

    <FieldSet labelText='Button'>
      <Button
        v-if="btnValue === 'Off'"
        v-bind:style='{ color: btnTxtColor, backgroundColor: btnBkgColor1 }'
        labelText='Off'
        :handleClick='onClick'
      />
      <Button
        v-if="btnValue === 'On'"
        v-bind:style='{ color: btnTxtColor, backgroundColor: btnBkgColor2 }'
        labelText='On'
        :handleClick='onClick'
      />
      {{ btnValue }}
    </FieldSet>

    <FieldSet labelText='TextBox'>
      <TextBox v-model='message1' placeholder='Edit Me' />
      <p>Message is: {{ message1 }}</p>
    </FieldSet>

    <FieldSet labelText='Number'>
      <Number v-model='num' placeholder='Edit Me' />
      <p>{{ num }}</p>
    </FieldSet>

    <FieldSet labelText='Search'>
      <Search v-model='searchText' placeholder='Edit Me' />
      <p>{{ searchText }}</p>
    </FieldSet>

    <FieldSet labelText='TextArea'>
      <TextArea v-model='message2' placeholder='Edit Me' />
      <p>Message is: {{ message2 }}</p>
    </FieldSet>

    <FieldSet labelText='Radio'>
      <Radio
        v-model='selectedValue'
        :options='options1'
        :selectedValue='selectedValue'
      />
      <p>Selected item is: {{ selectedValue }}</p>
    </FieldSet>

    <FieldSet labelText='CheckBox'>
      <CheckBox
        v-model='selectedValues'
        :options='options2'
        :selectedValues='selectedValues'
      />
      <p>Selected items is: {{ selectedValues.join(', ') }} </p>
    </FieldSet>

    <FieldSet labelText='Select'>
      <Select
        v-model='selectedItem'
        :options='options3'
        :selectedValue='selectedItem'
      />
      <p>Selected item is: {{ selectedItem }}</p>
    </FieldSet>

    <FieldSet labelText='Date'>
      <Date v-model='date' />
      {{ date }}
    </FieldSet>

    <FieldSet labelText='Time'>
      <Time v-model='time' />
      {{ time }}
    </FieldSet>

    <FieldSet labelText='Color'>
      <Color v-model='color' />
      {{ color }}
    </FieldSet>

    <FieldSet labelText='Range'>
      <Range v-model='range' />
      {{ range }}
    </FieldSet>

    <FieldSet labelText='Audio'>
      <Audio :src='src' />
    </FieldSet>
  </div>
</template>

<script>
import HeadLine from '../atoms/HeadLine.vue'
import FieldSet from '../atoms/FieldSet.vue'
import Button from '../atoms/Button.vue';
import TextBox from '../atoms/TextBox.vue'
import TextArea from '../atoms/TextArea.vue'
import Radio from '../atoms/Radio.vue'
import CheckBox from '../atoms/CheckBox.vue'
import Select from '../atoms/Select.vue';
import Date from '../atoms/Date.vue';
import Time from '../atoms/Time.vue';
import Color from '../atoms/Color.vue';
import Range from '../atoms/Range.vue';
import Audio from '../atoms/Audio.vue';
import Number from '../atoms/Number.vue';
import Search from '../atoms/Search.vue';

export default {
  components: {
    HeadLine,
    TextBox,
    Button,
    TextArea,
    FieldSet,
    Radio,
    CheckBox,
    Select,
    Date,
    Time,
    Color,
    Range,
    Audio,
    Number,
    Search
  },
  data() {
    return {
      btnValue: 'Off',
      message1: 'Hello, Text Box !',
      message2: 'Hello, Text Area !',
      num: 50,
      searchText: '',
      selectedValue: 'Orange',
      selectedValues: ['Blue'],
      options1: [
        { id: 'radio-0', groupName: 'fruits', value: 'Apple' },
        { id: 'radio-1', groupName: 'fruits', value: 'Orange' },
        { id: 'radio-2', groupName: 'fruits', value: 'Grape' },
      ],
      options2: [
        { id: 'checkbox-0', groupName: 'colors', value: 'Red' },
        { id: 'checkbox-1', groupName: 'colors', value: 'Green' },
        { id: 'checkbox-2', groupName: 'colors', value: 'Blue' },
      ],
      options3: [
        { id: 'typeA', value: 'A' },
        { id: 'typeB', value: 'B' },
        { id: 'typeO', value: 'O' },
        { id: 'typeAB', value: 'AB' },
      ],
      selectedItem: 'O',
      date: '2021-04-12',
      time: '12:00',
      color: '#e66465',
      range: 75,
      src: '',
      btnTxtColor: '#FBE9E7',
      btnBkgColor1: '#DD2C00',
      btnBkgColor2: '#00C853'
    }
  },
  methods: {
    onClick() {
      if (this.btnValue === 'Off') {
        this.btnValue = 'On';
      } else {
        this.btnValue = 'Off';
      }
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
