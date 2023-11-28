<script>
	export let data;
	import {HeaderKast, IntroKast, MobileMenu, NavDark, TheMaking, TheMaking2, TheMaking3, TheMaking4, Footer} from '$lib/index.js'
</script>

<NavDark />
<MobileMenu />
<HeaderKast {data} />
<IntroKast />
<TheMaking />
<TheMaking2 />
<TheMaking3 />
<TheMaking4 />
<Footer />

<style>
	/* .title-wrapper {
		height: 80vh;
	}

	h2 {
		font-size: 8vw;
	} */

	.filler {
		height: 60vh;
	}
</style>
