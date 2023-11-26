<script>
 export let data;   
</script>


			
			{#each data.stekjes as stekje}
				<article class={stekje.categories[0].naam}>
						<h3>{stekje.naam}</h3>
						<p><a href={stekje.slug}>Bekijk stekje</a></p>
					<img src={stekje.fotos[0].url} alt="foto van {stekje.naam}" />
				</article>
	        {/each}


<style>

	article{
		overflow: hidden;
		flex-direction: column;
		width: 15rem;
		height: 24rem;
		padding: 1rem;
		border-radius: 0.8rem;
	}

	article h3{
		color: white;
	}

	article a{
		color: white;
		text-decoration: none;
		background-color: orange;
		padding: 0.5rem;
		border-radius: 1rem;
		
	}

	 article img{
		position: relative;
		top: -10rem;
		left: -2rem;
		width: 18rem;
		height: 30rem;
		z-index: -1;
	 }


</style>
