<template>
  <div id="app" class="container">
    <h1>Harry Potter Elegant Housing</h1>
    <hr>
    <p>Welcome to {{ displayName }} a community where  {{displayDescription}}.</p>


      <button v-on:click="scrambleHouses" id="sortButton" type="button" class="btn btn-primary">New House</button>

  </div>
</template>

<script>

var displayName = '';
var displayDescription = '';
var scrambleHouses = '';
import house from './components/house.vue';

export default {
  name: 'app',
  components : {
    house
  },
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
    
    methods: {
      scrambleHouses : function() {
      // console.log(this.Houses);
      var json = this.Houses;
      //console.log(json.length);
      //console.log(json);
      var rando = Math.floor(Math.random()*json.length);
      //console.log(rando);
      var house = this.Houses[rando];
      console.log(house.name);
      console.log(house.description);
      this.displayName = house.name;
      this.displayDescription = house.description;

      }
    },
    created : function() {
    return scrambleHouses;
    }


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
