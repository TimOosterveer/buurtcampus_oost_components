<script>
	export let data;
	console.log(data);
</script>

{#each data.workshops as workshop}
	<section>
		<img src={workshop.foto[0].url} alt="" />

		<h2>{workshop.naam}</h2>
	</section>
{/each}

<style>
	section {
		position: relative;
		border-radius: var(--bradius);
		height: 40rem;
    margin: var(--margin);
	}

  
	img {
    position: absolute;
    border-radius: var(--bradius);
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    object-fit: cover;
    z-index: -1;
  }
  
  h2 {
    color: white;
  }

</style>
