<script>
	import StekjeCard from '$lib/atoms/StekjesCard.svelte';
	import Footer from '$lib/organisms/Footer.svelte';
	import Navigation from '$lib/organisms/NavDark.svelte';
	import MobileNavigation from '$lib/organisms/MobileMenu.svelte';
	export let data;
</script>

<header>
	<Navigation></Navigation>
	<MobileNavigation></MobileNavigation>
</header>

<!-- hier komt nog tekst -->
<main>
	{#each data.stekjes as stekje}
		<StekjeCard {data}></StekjeCard>
	{/each}
</main>

<Footer></Footer>

<style>
	header {
		margin-bottom: 5rem;
	}

	main {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: center;
		gap: 1rem 1.5rem;
		margin: 2rem;
	}
</style>
