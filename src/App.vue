<template>
  <div>{{greet}} {{name}}</div>
  <div v-html="career"></div>
  <!-- <div v-html="hack"></div> -->
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 class="underline" v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isSoldOut ? 'sold-out' : 'new'">Sold Out Movie</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly Promoted Movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">Array Conditional Movie</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldOut,
  }">Object Conditional Movie</h2>
  <h2 v-bind:style="{
    color: highlightColor,
    'font-size': headerSize + 'px',
    padding: '20px',
  }">Inline Style</h2>
  <h2 v-bind:style="headerStyleObject">Style Object</h2>

</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      greet: "Hello",
      name: "HamsoAce",
      career: "<b>Software Dev</b>",
      // hack: `<a href="github.com/hamsoace" onclick="alert('You have been hacked!')">Win a prize!</a>`,
      headingId: 'heading',
      isDisabled: false,
      status: 'success',
      isPromoted: true,
      isSoldOut: true,
      highlightColor: 'blue',
      headerSize: 30,
      headerStyleObject: {
        color: 'yellow',
        fontSize: '25px',
        padding: '30px',

      }
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

.promoted{
  font-style: italic;
}

.underline{
  text-decoration: underline;
}

.sold-out{
  color: red;
}

.new{
  color: aqua;
}

</style>
