<template>
  <div id="myheader">
    
    <div class="row">
    <div class="col-sm-4">
      <img src="./../assets/talkinghat.png">
    </div>
    <div class="cal-sm-8">
      <h3>Hocus Pocus</h3>
      <h1>Talking Hat</h1>      
    </div>
    </div>
    
    <hr>


  </div>
</template>

<script>




export default {
  name: 'myheader',
  components : {
    
  }, 

  };  

</script>

<style>

#myheader {
  margin-left: 20px;
  color: blue;
}

h1, h3 {
  text-align: center;
  font-family: 'Anton', sans-serif;
  color: #56A902;
  padding-left: 20px;
  letter-spacing: 3px;
  font-size: 50px;
}

img {
  height: 100%;
  width:100%;
}

</style>