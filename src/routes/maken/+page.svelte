<script>
	import IntroKast from '$lib/organisms/IntroKast.svelte';
	import MobileMenu from '$lib/organisms/MobileMenu.svelte';
	import NavDark from '$lib/organisms/NavDark.svelte';
	import TheMaking from '$lib/organisms/TheMaking.svelte';
	import TheMaking2 from '$lib/organisms/TheMaking2.svelte';
	import TheMaking3 from '$lib/organisms/TheMaking3.svelte';
	import TheMaking4 from '$lib/organisms/TheMaking4.svelte';
	import Footer from '$lib/organisms/Footer.svelte';
</script>

<NavDark />
<MobileMenu />
<IntroKast />
<TheMaking />
<TheMaking2 />
<TheMaking3 />
<TheMaking4 />

<div class="filler"></div>
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