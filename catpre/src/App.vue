<template>
  <div id="app">
    <button v-on:click="addCount()">點我+1</button>
    <button @click="addCount1()">點我+2</button>
    <p>{{ count }}</p>
  </div>
</template>

<script>
export default {
  data(){
    return{
      count:0
      }
    },
    methods:{
      addCount:function(){
        this.count += 1;
      },
      addCount1:function(){
        this.count += 2;
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
