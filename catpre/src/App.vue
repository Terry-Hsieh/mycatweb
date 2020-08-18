<template>
<div id="app">
    <!-- No modifiers -->
    <div @click="firstFunction()">
        <div @click="secondFunction()">
            <p>
                沒有修飾符：
                <button @click="thirdFunction()">點我</button>
            </p>
        </div>
    </div>
    
    <!-- Add .stop modifiers -->
    <div @click="firstFunction()">
        <div @click="secondFunction()">
            <p>
                加入.stop修飾符：
                <button @click.stop="thirdFunction()">點我</button>
            </p>
        </div>
    </div>
    
    <!-- Add .prevent modifiers -->
    <div>
        <form method="POST">
            <span>瀏覽器預設行為會跳轉頁面：</span>
            <input type="text" placeholder="input something">
            <button>Submit</button>
        </form>
        <form method="POST">
            <span>加入.prevent修飾符：</span>
            <input type="text" placeholder="input something">
            <button @click.prevent>Submit</button>
        </form>
    </div>
    
    <!-- Add .capture modifiers -->
    <div @click.capture="firstFunction()">
        <div @click.capture="secondFunction()">
            <p>
                加入.capture修飾符：
                <button @click.capture="thirdFunction()">點我</button>
            </p>
        </div>
    </div>
    
    <!-- Add .self modifiers -->
    <div class="outerDiv" @click.self="firstFunction()">
        <div class="middleDiv" @click.self="secondFunction()">
            <p>
                加入.self修飾符：
                <button @click="thirdFunction()">點我</button>
            </p>
        </div>
    </div>
    
    <!-- Add .once modifiers -->
    <div>
        <p>
            正常執行計數function：
            <button @click="addCount1()">點我+1</button> {{ count1 }}
             
            加入.once修飾符：
            <button @click.once="addCount2()">點我+1</button> {{ count2 }}
        </p>
    </div>
</div>
</template>

<script>
export default {
  data(){
    return{
      count1:0,
      count2:1
      }
    },
    methods:{
      thirdFunction () {
            alert('thirdFunction() is called.');
        },
      secondFunction () {
            alert('secondFunction() is called.');
        },
        firstFunction () {
            alert('firstFunction() is called.');
        },
        addCount1 () {
            this.count1 += 1;
        },
        addCount2 () {
            this.count2 += 1;
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
