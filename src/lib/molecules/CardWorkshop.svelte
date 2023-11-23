<script>
	export let data;
	console.log(data);
</script>

{#each data.workshops as workshop}
	<section>
    <img src={workshop.foto[0].url} alt="">

   

        <h2>{workshop.naam}</h2>
  </section>
{/each}



<style>

  section {
    position: relative;
    border-radius: var(--bradius);
    height: 40rem;
    padding: var(--padding);
  }

  
  /* section::after {
    content: '';
		position: absolute;
		background-color: #2b2b2b;
    border-radius: var(--bradius);
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		opacity: .4;
		z-index: 0;
  } */
  
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: var(--bradius);
  }

  section::after {
    content: '';
		position: absolute;
		background-color: #2b2b2b;
    border-radius: var(--bradius);
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		opacity: .4;
		z-index: 0;
    margin: 2rem;
  }  
</style>