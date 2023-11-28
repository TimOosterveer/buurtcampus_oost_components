<script>
 export let data;   
</script>
                                               

			
			
				<article class={data.stekjes[0].categories[0].naam}>
						<h3>{data.stekjes[0].naam}</h3>
						<span><a href={data.stekjes[0].slug}>Bekijk stekje <i class="fa-solid fa-play" style="color: #ffffff;"></i></a></span>
					<img src={data.stekjes[0].fotos[0].url} alt="data.stekjes[0].naam" />
				</article>                                                                                                                                                                                                                                                                                                                                                           


<style>

	article{
		overflow: hidden;
		width: 13rem;
		height: 22rem;
		padding: 1.5rem;
		border-radius: var(--bradius);
	}


	article h3{
		color: white;
	}

	article span{
		position: relative;
		width: 6rem;
		background-color: var(--button-color);
		padding: 6px;
		border-radius: 1rem;
		top: 15.5rem;
	}

	article a{
		text-decoration: none;
		color: white;
	}

	


	 article img{
		position: relative;
		top: -10rem;
		left: -2rem;
		width: 18rem;
		height: 30rem;
		z-index: -2;
	 }


</style>
