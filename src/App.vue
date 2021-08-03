<template>
  <div>{{greet}} {{name}}</div>
  <div v-html="career"></div>
  <div v-html="hack"></div>
  <button v-bind:disabled="isDisabled">Bind</button>

</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      greet: "Hello",
      name: "HamsoAce",
      career: "<b>Software Dev</b>",
      hack: `<a href="github.com/hamsoace" onclick="alert('You have been hacked!')">Win a prize!</a>`,
      headingId: 'heading',
      isDisabled: false,
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
