<template>
	
	<div id="questions">
		<p>testing for qs</p>
		<button v-on:click="answerQs" id="sortButton" 
	       	type="button" class="btn"></button>
		
	</div>

</template>

<script>
	
	export default {
		name : 'questions',
		props : [ 'house' ],
	    data: function() {
	      return {
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
	  methods : {
	  	answerQs : function() {
	  		var qs = this.Questions;
	  		console.log(qs);
	  	}
	  }
	}  

</script>

<style>
	

</style>