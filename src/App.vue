<template>
  <div id="app">
    <h1>Harry Potter Magic Land</h1>
    
    <!-- <p>{{house}}</p> -->


    <!-- <button v-on:click="randomHouse" id="sortButton" type="button" class="btn btn-primary">New House</button>
  -->

  <!-- <ul>
      <li v-for="House in Houses">
       <p> Welcome to {{ House.name }} a home where {{House.description}}.</p>
    </li> -->
    <!--  <li v-for="House in Houses">
        {{ de.name }}
    </li> -->
 <!--  </ul> -->

  </div>
</template>

<script>

export default {
  name: 'app',
  data: function() {
      return {
      Houses : [
        {
          name: 'Gryffindor',
          description: 'magic happens'
        },
        {
          name: 'Hufflepuff',
          description: 'things blow up'
        },
        {
          name: 'Ravenclaw',
          description: 'we claw you when you enter'
        },
        {
          name: 'Slytherin',
          description: 'snakes are our pets'
        }

      ],

      'Questions': [

        { 
          text: 'What is your favorite color?',
          answers: [
            {
              text: 'Scarlet',
              house: 'Gryffindor'
            },
            {
              text: 'Yellow',
              house: 'Hufflepuff'
            },
            {
              text: 'Blue',
              house: 'Ravenclaw'
            },
            {
              text: 'Green',
              house: 'Slytherin'
            }
          ]
        },
        { 
          text: 'What is your favorite animal?',
          answers: [
            {
              text: 'Lion',
              house: 'Gryffindor'
            },
            {
              text: 'Badger',
              house: 'Hufflepuff'
            },
            {
              text: 'Eagle',
              house: 'Ravenclaw'
            },
            {
              text: 'Snake',
              house: 'Slytherin'
            }
          ]
        },
        { 
          text: 'What kind of person do you try to be?',
          answers: [
            {
              text: 'Brave',
              house: 'Gryffindor'
            },
            {
              text: 'Loyal',
              house: 'Hufflepuff'
            },
            {
              text: 'Witty',
              house: 'Ravenclaw'
            },
            {
              text: 'Cunning',
              house: 'Slytherin'
            }
          ]
        },
        { 
          text: 'Who is your favorite witch or wizard?',
          answers: [
            {
              text: 'Albus Dumbledore',
              house: 'Gryffindor'
            },
            {
              text: 'Newt Scamander',
              house: 'Hufflepuff'
            },
            {
              text: 'Garrick Ollivander',
              house: 'Ravenclaw'
            },
            {
              text: 'Tom Riddle',
              house: 'Slytherin'
            }
          ]
        },
        { 
          text: 'What is your favorite Berty Bott\'s flavor?',
          answers: [
            {
              text: 'Grape',
              house: 'Gryffindor'
            },
            {
              text: 'Horseradish',
              house: 'Hufflepuff'
            },
            {
              text: 'Roast Beef',
              house: 'Ravenclaw'
            },
            {
              text: 'Spinach',
              house: 'Slytherin'
            }
          ]
        }

      ]
    };
  },
    created : function() {
      // console.log(this.Houses);
      var json = this.Houses;
      //console.log(json.length);
      //console.log(json);
      var rando = Math.floor(Math.random()*json.length);
      //console.log(rando);
      var house = this.Houses[rando];
      console.log(house.name);
      console.log(house.description);
      }


    // var randomnum = Math.floor((Math.random() * 3));
    // console.log(json[randomnum].first_name);
      
      //var rando = items[Math.floor(Math.random()*items.length)];
    

    // scramble : function (){
    //   alert('Welcome to the sorting hat!!!!')
    // },
    // beforeMount(){
    // this.scramble();
  //}
  
 };


</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
  margin-left: 30px;
}

h1, h2 {
  font-weight: normal;
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
