<script>
	export let data;
	import { HeaderStekje, Footer, NavDark, MobileMenu, StekjeCard } from '$lib/index.js';
</script>

<NavDark />
<MobileMenu />

<HeaderStekje {data} />

<!-- hier komt nog tekst -->
<main>
	{#each data.stekjes as stekje}
		<StekjeCard {data}></StekjeCard>
	{/each}
	<!-- <StekjesCard data={data}/> -->
</main>

<Footer />

<style>
	/* header {
		margin-bottom: 5rem;
	} */

	main {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		/* justify-content: center; */
		gap: 1rem 1.5rem;
		margin: 2rem;
	}
</style>
