<script>
	let firstName = "";
	let lastName = "";	
	let src = "favicon.png";
	// let count = 0;
	// const incrementCounter = () =>{
	// 	count += 1;
	// }
	// const handleInput = (a) =>{
	// 	name = a.target.value;
	// }
	// const resetName=()=>{
	// 	name = "Unknown";
	// }

	$ : fullName = `${firstName} ${lastName}`	

</script>

<main>
	<h1>Hello {fullName}</h1>
	<label for="firstName">First Name</label>
	<input type="text" bind:value={firstName}>
	<label for="lastName">Last Name</label>
	<input type="text" bind:value={lastName}>
	
	<img src={src} alt ="Svelte Logo">
		
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;

	}
	h1{
		font-size: 72px;
		text-align: center;
	}
	
	
</style>