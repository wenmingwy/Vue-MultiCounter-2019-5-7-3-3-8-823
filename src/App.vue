<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <br>
    <input type="text" v-model="input1" placeholder="">
    <div v-if="parseInt(input1)%1==0 && parseInt(input1)>=0">
      <Counter v-for="n in parseInt(input1)" 
       v-bind:key="n" 
       v-bind:index="n"
       v-on:update="sum += $event"/>
    </div>
    <div v-else>
        <Counter v-for="n in 0"  v-bind:key="n" v-bind:index="n"/>
    </div>
    sum:{{sum}}
  </div>
</template>

<script>
import Counter from './components/Counter.vue'

export default {
  name: 'app',
  components: {
    Counter
  },
  data(){
    return {
      input1 : 0,
      sum : 0
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
