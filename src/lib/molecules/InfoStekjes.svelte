
<script>
	import Vector from '$lib/assets/vector.svg';
	import VectorPlant from '$lib/assets/vectorplant.svg';

</script>

<div class="info-workshop">
	<div class="vector">
		<img src={Vector} alt="icon info tekst" />
	</div>

<p>Heb jij een of meerdere plantenstekjes over en zou je die graag willen ruilen voor een nieuwe plantje? Bekijk hieronder ons aanbod.</p>

	<div class="info-paragraph">
		<img id="one" src={VectorPlant} alt="incon plant" />
		<img id="two" src={VectorPlant} alt="incon plant" />
		<img id="three" src={VectorPlant} alt="incon plant" />
	</div>

</div>

<style>
	.info-workshop {
		position: relative;
		display: flex;
		gap: var(--padding);
		background-color: var(--background-color-light);
		border-radius: var(--bradius);
		height: 11rem;
		padding: var(--padding);
		overflow: hidden;
	}

   .info-workshop p{
        z-index: 10;
       
    }

	.info-paragraph {
		width: 60%;
	}

	#one {
		position: absolute;
		top: 10rem;
		right: 18rem;
	}

	#two {
		position: absolute;
		top: -150px;
		right: 10rem;
		transform: rotate(250deg);
	}
	#three {
		position: absolute;
		top: 6rem;
		right: -7rem;
		transform: rotate(-10deg);
	}
</style>


