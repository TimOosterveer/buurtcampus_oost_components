<script>
	export let data;
	import { HeaderStekje, Footer, NavDark, MobileMenu, StekjeCard, StekjesInfo } from '$lib/index.js';
</script>

<NavDark />
<MobileMenu />
<HeaderStekje {data} />

<main>
	<div class="intro">
		<StekjesInfo/>
	</div>
	{#each data.stekjes as stekje}
		<StekjeCard {data} />
	{/each}
	<!-- <StekjesCard data={data}/> -->
</main>

<Footer />

<style>
	.intro {
		width: 13rem;
		height: 22rem;
		background-color: var(--card-color-light);
		border-radius: var(--bradius);
	}


	main {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		justify-content: center;
		gap: 1rem 1.5rem;
		margin: 1rem;
		margin-top: 3rem;
	}
</style>
