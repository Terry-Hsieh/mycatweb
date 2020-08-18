<template>
  <div id="app">
    <ul class="menulist">
      <li><a href="https://www.google.com/search?q=laptop&oq=laptop&aqs=chrome..69i57j0l7.4134j0j7&sourceid=chrome&ie=UTF-8" :style="styleObject">home</a></li>
      <li><a href="#">about</a></li>
      <li><a href="#">work</a></li>
      <li><a href="#">contact</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      styleObject:{
          color: '#2c3e54',
          fontSize:'20px'
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
