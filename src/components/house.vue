<template>
	
	<div id="house">

		<p>Welcome to {{ displayName }} a community where  {{displayDescription}}.</p>

	    <button v-on:click="reload" id="sortButton" 
	       	type="button" class="btn">Too cool for {{displayName}}?</button>

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
		  	},
			methods : {
				reload : function () {
					location.reload();
					}
			},
	}

</script>

<style>
	
	#house {
		margin : 5px;
		border : 10px solid #3B4E32;
		width : 100%;
		height : auto;
		min-height: 200px;
		position: center;
		text-align: center;
		padding-top: 30px;		
		background-color : #F8F8FF;
	}

	.btn {
		background-color: #56A902;
		padding-top: 6px;
	}

	p {
		margin: 10px;
		padding-bottom: 10px;
	}

</style>