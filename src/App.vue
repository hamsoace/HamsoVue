<template>
  <!-- Forms -->
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form action="">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name">
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea name="" id="profile" cols="30" rows="10" v-model="formValues.profileSummary"/>
    </div>
  </form>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      formValues:{
        name: '',
        profileSummary: ''
      }
    }
  },
  methods: {
    
    },
 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

label{
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label{
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type = 'text'],
textarea,
select{
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}

</style>
