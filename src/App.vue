<template>

  <div id="app">
    
    <myheader/>
    <house></house>   

  </div>

</template>

<script>


import house from './components/house.vue';
import myheader from './components/myheader.vue';
import questions from './components/questions.vue';

export default {
  name: 'app',
  components : {
    house,
    myheader,
    questions
  }, 

  };  

</script>

<style>
#app {
  padding-top: 20px;
  margin-left: 30px
}



</style>