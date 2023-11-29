<script>
	import ContactForm from '$lib/molecules/ContactForm.svelte';
	import Location from '$lib/atoms/Location.svelte';
	import Footer from '$lib/organisms/Footer.svelte';
	import Navigation from '$lib/organisms/NavDark.svelte';
	import MobileNavigation from '$lib/organisms/MobileMenu.svelte';
</script>

<header>
	<MobileNavigation />
	<Navigation />
</header>

<main>
	<ContactForm />
	<Location />
</main>

<Footer />

<style>


	main {
		margin: var(--margin);
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		gap: 2rem;
		padding: var(--padding);
		background-color: var(--background-color-light);
		border-radius: var(--bradius);
	}
</style>
