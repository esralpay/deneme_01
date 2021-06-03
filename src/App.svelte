<script>
import Announcement from "./Announcement.svelte";

	let fruits =[
		{name:"Apple",color:"red",amount:5,id:1},
		{name:"Banana",color:"yellow",amount:7,id:2},
		{name:"Grape",color:"purple",amount:3,id:3},
		
	];
	const deleteFruit = (id) =>{
		fruits = fruits.filter((fruit)=>fruit.id != id)
		console.log(fruits);
	}	

</script>

<main>
	<Announcement/>
	{#each fruits as fruit(fruit.id)}
		{#if fruit.amount < 4}
			<div class ="card">
				<h5>{fruit.name}</h5>
				<p>{fruit.color}</p>
				<button on:click={()=> deleteFruit(fruit.id)}>Delete</button>
			</div>
		{:else}
			<p>The amount of {fruit.name} is greater or equal to 4.</p>
		{/if}
	{/each}
		
</main>

<style>
	.card {
		min-width: 400px;
		padding:8px;
		border-radius: 20px;
		border: 2px solid gray;
		margin-top: 8px;
		

	}

	h5,p{
		margin: 8px, 0px;
	}
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-top: 8px;

		
	}
	
	
</style>