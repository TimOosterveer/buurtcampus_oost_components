<script>
	// export let data;
	// console.log(data);

	import { onMount } from 'svelte';

	// let selectedMaintenance = 'Alle';

	// // Functie om de stekjes te filteren op onderhoudsniveau
	// function filterStekjes(stekje) {
	// 	if (selectedMaintenance === clickt) {
	// 		return true; // Toon alle stekjes als 'Alle' is geselecteerd
	// 	} else {
	// 		return stekje.onderhoud === selectedMaintenance;
	// 	}
	// }
	let selected = ['makkelijk', 'uitdagend'];
	const onderhouds = ['makkelijk', 'uitdagend	'];
	
	
	let filteredWorkshops = data.stekjes // Data van de workshops in filteredWorkshops
	
	console.log(filteredWorkshops)
	function filterWorkshops() {
		if (selected) {
			filteredWorkshops = stekjes.onderhoud.filter((ond) => {
				console.log(filteredWorkshops)
				return ond.onderhoud.toLowerCase().includes(selected.toLowerCase());
			});
		} else {
			filteredWorkshops = data.stekjes;
		}
	}
	// onMount(() => {
	// });
</script>


<form on:submit|preventDefault={filterWorkshops}>
	<label for="month">Selecteer maand:</label>
	<select id="month" bind:value={selected} on:change={filterWorkshops}>
		<option value="">alle</option>
		{#each onderhouds as month}
			<option value={month}>{month}</option>
		{/each}
	</select>
</form>

<section class="wrapper">
	{#each filteredWorkshops as stekje}
		<a href={stekje.slug}>
			<article>
				<img src={stekje.fotos[0].url} alt="foto van {stekje.naam}" />
				<div>
					<h3>{stekje.naam}</h3>
					<p>{stekje.onderhoud}</p>
				</div>
			</article>
		</a>
	{/each}
</section>
<style>
	select {
		display: flex;
		flex-direction: column;
		width: 10rem;
    padding: 0.5rem;
    border-radius: 0;
    border: 2px solid #4D7141;
	}

  select:focus {
    border: 3px solid rgb(17, 84, 255);
  }
</style>    
