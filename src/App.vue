<template>
  <div id='app'>
    <span>
      <router-link to='/'>
        <Button labelText='Home' :handleClick='onClick1' />
      </router-link>
      <router-link to='/about'>
        <Button labelText='About' :handleClick='onClick2' />
      </router-link>
    </span>
    <router-view/>
  </div>
</template>

<script>
import Button from './atoms/Button.vue'

export default {
  components: {
    Button
  },
  methods: {
    onClick1() { console.log('home'); },
    onClick2() { console.log('about'); }
  }
}
</script>

<style>
#app {
  margin: 10px;
  padding: 10px;
}
</style>
