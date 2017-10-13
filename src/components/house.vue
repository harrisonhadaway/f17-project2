<template>
	
	<div
	class="house">
		<p>Welcome {{ displayName }}</p>
	</div>

</template>

<script>
	
	export default {
		name : 'house',
		props : [ 'displayName'],
		methods : {
			
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