<template>
  <div>
    <span>{{index}}</span>  
    <p>number is {{number}}</p>
    <button @click="inc">+</button>&emsp;&emsp;
    <button @click="dec">-</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number:0
    };
  },
  props:{
      index : Number
  },
  created:function(){
    this.$emit('update',this.number);
  },
  destroyed:function(){
    this.$emit('update',-this.number);
  },
  methods: {
    inc() {
      this.number++;
      this.$emit("update",1);
    },
    dec() {
      this.number--;
      this.$emit("update",-1);
      }
    },
  }
 
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
