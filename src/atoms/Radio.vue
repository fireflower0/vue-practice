<template>
  <div>
    <div class='form-wrapper' v-for='option in options' v-bind:key='option.id'>
      <input
        type='radio'
        v-model='option.checked'
        :id='option.id'
        :checked='option.checked'
        :name='option.groupName'
        :value='option.value'
        @change='setValue'
      />
      <label :for='option.id'>{{ option.value }}</label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Radio',
  props: {
    value: String,
    name: String,
    options: Array
  },
  methods: {
    setValue (e) {
      this.$emit('input', e.target.value);
    }
  }
}
</script>

<style scoped>
.form-wrapper {
  margin: 5px;
  float: left;
}
.form-wrapper input {
  display: none;
}
.form-wrapper label {
  display: block;
  width: 100px;
  text-align: center;
  cursor: pointer;
  border: 1px solid #263238;
  border-radius: 5px;
  background-color: #ECEFF1;
}
.form-wrapper input:checked + label {
  background-color: #00E676;
}
</style>
