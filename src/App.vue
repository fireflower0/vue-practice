<template>
  <div id='app'>
    <span>
      <router-link to='/'>
        <Button
          v-bind:style='{ color: btnTxtColor, backgroundColor: btnBkgColor }'
          labelText='Home'
          :handleClick='onClick1'
        />
      </router-link>
      <router-link to='/about'>
        <Button
          v-bind:style='{ color: btnTxtColor, backgroundColor: btnBkgColor }'
          labelText='About'
          :handleClick='onClick2'
        />
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
  data() {
    return {
      btnTxtColor: '#263238',
      btnBkgColor: '#69F0AE'
    }
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
