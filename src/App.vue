<template>
  <h2 v-if="num === 0">The Number is Zero</h2>
  <h2 v-else-if="num < 0">The Number is Negative</h2>
  <h2 v-else-if="num > 0">The Number is Positive</h2>
  <h2 v-else>Not a Number</h2>

  <div v-if="display">
    <h2>Hamisi</h2>
    <h2>Software Dev</h2>
    <h2>Vue</h2>
  </div>
  
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      num: -10,
      display: true,
    }
  }
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
