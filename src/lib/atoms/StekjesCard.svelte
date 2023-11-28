<script>
	import Button from "$lib/atoms/ButtonStekje.svelte"
	export let data;
</script>


<article class={data.stekjes[0].categories[0].naam}>
	<h3>{data.stekjes[0].naam}</h3>
	<p><a href={data.stekjes.slug}>Bekijk stekje</a></p>
	<img src={data.stekjes[0].fotos[0].url} alt="data.stekjes[0].naam" />
</article>



<style>
	article {
		overflow: hidden;
		width: 13rem;
		height: 22rem;
		padding: 1.5rem;
		border-radius: 1rem;
	}

	article h3 {
		color: white;
	}

	article a {
		position: relative;
		color: white;
		text-decoration: none;
		background-color: orange;
		padding: 0.4rem;
		border-radius: 1rem;
		top: 15.5rem;
	}

	article img {
		position: relative;
		top: -10rem;
		left: -2rem;
		width: 18rem;
		height: 30rem;
		z-index: -2;
	}
</style>
