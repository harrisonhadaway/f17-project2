<template>
	
	<div
	class="house">
		 <p>Welcome to {{ displayName }} a community where  {{displayDescription}}.</p>
	</div>

</template>

<script>
	
var displayName = '';
var displayDescription = '';

	export default {
		name : 'house',
		props : [],
		data : function() {
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
	  	this.displayName = house.name;
	  	this.displayDescription = house.description;
	  	}
		}

	

</script>

<style>
	
	/*.house {
		margin : 5px;
		border : 2px solid #000;
		width : 500px;
		height : 100px;
		position: center;		
		background-color : #ccc;
	}*/

</style>