<template>
  <!-- Event Handling -->
  <h2>{{name}}</h2>
  <div>
    <button @click="changeName($event), increment(1, $event)">Change Name</button>
  </div>

  <h2>{{count}}</h2>
  <div>
    <button @click="increment(20, $event)">Increment</button>
    <button @click="increment(15)">Increment</button>
    <button @click="decrement(10)">Decrement</button>
    <button @click="decrement(5)">Decrement</button>
  </div>

</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      name: 'Hamisi',
      count: 0
    }
  },
  methods: {
    changeName(event){
      this.name = 'Batman'
      console.log('Event', event)
    },
    increment(num, event){
      this.count += num
      console.log('Event', event)
    },
    decrement(num){
      this.count -= num
    },
    },
 
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
