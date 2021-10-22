<template>
  <div id="app">
    <Sign />
    <Shelves />
    <TextBox />
  </div>
</template>

<script>
import Sign from './components/Sign.vue'
import Shelves from './components/Shelves.vue'
import TextBox from './components/TextBox.vue'

export default {
  name: 'App',
  components: {
   TextBox,
    Shelves,
    Sign
  }
}
</script>

<style>
html,body{
  margin: 0;
}
#app{
  /* background-image: url('./assets/background.svg'); */
  background-color: black;
  height: 100vh;
}
</style>
