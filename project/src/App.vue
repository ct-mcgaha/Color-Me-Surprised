<template>
  <div id="app">
    <color-me-surprised />  
    </div>
</template>

<script>
import ColorMeSurprised from './components/ColorMeSurprised.vue'

export default {
  name: 'App',
  components: {
        ColorMeSurprised
  }
}
</script>

<style>
#app {
  font-family:'Times New Roman', Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 48px;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
