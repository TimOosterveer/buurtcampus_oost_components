<script>
	 import StekjesInfo from '$lib/molecules/InfoStekjes.svelte';
	export let data;
</script>

<StekjesInfo/>
{#each data.stekjes as stekje}
	<article class={stekje.categories.naam}>
		<img src={stekje.fotos[0].url} alt="" />
		<a href={stekje.slug}>Bekijk stekje <i class="fa-solid fa-play" style="color: #ffffff;"></i></a>
		<h3>{stekje.naam}</h3>
	</article>
{/each}

<style>
	article {
		position: relative;
		width: 24.2%;
		height: 70vh;
		padding: 1rem;
		border-radius: var(--bradius);
		overflow: hidden;
		margin-top: 1rem;
	}

	h3 {
		position: relative;
		color: white;
		z-index: 5;
		font-size: 2rem;
		line-height: 1.5em;
	}

	article a {
		position: absolute;
		bottom: 1rem;
		left: 1rem;
		text-decoration: none;
		color: white;
		background-color: var(--button-color);
		padding: 0.5rem 1rem;
		border-radius: var(--bradius);
		cursor: pointer;
		z-index: 5;
		transition: 0.2s;
	}

	a:hover {
		background-color: white;
		color: var(--button-color);
	}

	img {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		z-index: 1;
		object-fit: cover;
	}

	img::after {
		position: absolute;
		left: 0;
		top: 0;
		height: 100%;
		width: 100%;
		content: '';
		background-color: rgba(0, 0, 0, 0.753);
		z-index: 3;
	}
</style>
