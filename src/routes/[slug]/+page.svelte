<script>
	export let data;
</script>

<section class="image-section">
	<img src={data.stekje.fotos[0].url} alt="foto van {data.naam}" />
	<h1>{data.stekje.naam}</h1>
</section>

<section class="container">
	<div class="stekje-container">
		<div class="left">

		<h2>Beschrijving</h2>
		<p>{data.stekje.beschrijving}</p>
	</div>
	<div class="right">
		<ul class="accordion">
			<li>
				<input type="radio" name="accordion" id="first" checked />
				<label for="first">Landherkomst</label>
				<div class="content">
					<p>{data.stekje.landvanherkomst}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="second" />
				<label for="second">Voeding</label>
				<div class="content">
					<p>{data.stekje.voeding}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="fifth" />
				<label for="fifth">Temperatuur</label>
				<div class="content">
					<p>{data.stekje.temperatuur}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="fourth" />
				<label for="fourth">Giftig</label>
				<div class="content">
					<p>{data.stekje.giftig}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="third" />
				<label for="third">Verpotten</label>
				<div class="content">
					<p>{data.stekje.verpotten}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="sixth" />
				<label for="sixth">Watergeven</label>
				<div class="content">
					<p>{data.stekje.watergeven}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="seventh" />
				<label for="seventh">Zonlicht</label>
				<div class="content">
					<p>{data.stekje.zonlicht}</p>
				</div>
			</li>

			<li>
				<input type="radio" name="accordion" id="eighth" />
				<label for="eighth">Stekken</label>
				<div class="content">
					<p>{data.stekje.stekken}</p>
				</div>
			</li>
		</ul>
	</div>
</section>

<style>
	section {
		position: relative;
		width: 100%;
		background-color: var(--background-color);
	}

	.image-section {
		height: 90vh;
	}

	img {
		object-fit: cover;
		width: 100%;
		height: 100%;
	}

	h1 {
		position: absolute;
		bottom: 2rem;
		left: 2rem;
		color: white;
		font-size: 5vw;
	}

	h2 {
		color: var(--background-color);
		font-size: 3vw;
	}

	.container {
		padding: 2rem;
	}

	.stekje-container {
		position: relative;
		background-color: var(--card-color-light);
		width: 100%;
		border-radius: var(--bradius);
		display: flex;
		padding: 2rem;
		justify-content: space-between;
	}

	.left {
		position: sticky;
		top: 0;
		width: 40%;
		height: 89vh;
		padding-right: 10%;
	}

	.right {
		width: 50%;
		padding: 0;
	}

	.accordion {
		width: 100%;
		border-radius: var(--bradius);
	}

	.accordion li {
		list-style: none;
		padding: 10px;
		display: flex;
		flex-direction: column;
		margin-bottom: 1rem;
		width: 100%;
		background-color: var(--button-color);
		border-radius: var(--bradius);
	}

	.accordion li label {
		display: flex;
		align-items: center;
		color: var(--background-color);
		text-transform: uppercase;
		padding: 10px;
		cursor: pointer;
	}

	label::before {
		content: '+';
		color: var(--card-color-light);
		font-size: 24px;
		font-weight: 500;
	}

	input[type='radio'] {
		display: none;
	}

	.accordion .content {
		color: white;
		padding: 0 10px;
		line-height: 26px;
		max-height: 0;
		overflow: hidden;
		transition:
			max-height 0.5s,
			padding 0.5s;
	}

	.accordion input[type='radio']:checked + label + .content {
		max-height: 400px;
		padding: 10px 10px 20px;
	}
</style>
