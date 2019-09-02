<template>
  <div>
    <p>number is {{number}}</p>
    <button @click="inc">+</button>&emsp;&emsp;
    <button @click="dec">-</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 0
    };
  },
  methods: {
    inc() {
      const number = this.number;
      this.number++;
    },
    dec() {
      const number = this.number;
      this.number--;
      }
    }
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
