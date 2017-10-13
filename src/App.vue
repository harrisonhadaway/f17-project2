<template>
  <div id="app" class="container">
    <h1>Harry Potter Elegant Housing</h1>
    <hr>
    <house/>


      <!-- <button v-on:click="scrambleHouses" id="sortButton" type="button" class="btn btn-primary">New House</button> -->

  </div>
</template>

<script>


import house from './components/house.vue';

export default {
  name: 'app',
  components : {
    house
  }, 

  };  

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: ;
  margin-top: 60px;
  margin-left: 30px;
}

h1 {
  font-weight: normal;
  font-family: 'Anton', sans-serif;
}

h2 {
  font-weight: lighter;
  font-family: 'Open Sans Condensed', sans-serif;
  padding-top: 10%;
  text-align: center;
}

ul {
  list-style-type: none;
  align-content: left;
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
