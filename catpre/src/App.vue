<template>
  <div id="app">
    <select v-model="selected">
        <option value="123">Item1</option>
        <option value="456">Item2</option>
        <option value="789">Item3</option>
    </select>
    <div>selected = {{ selected }}</div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      selected:null
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
