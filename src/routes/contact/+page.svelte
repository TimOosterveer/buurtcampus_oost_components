<script>
    import  ContactForm from '$lib/molecules/ContactForm.svelte'
    import Location from '$lib/atoms/Location.svelte'
    import Footer from '$lib/organisms/Footer.svelte'
     import Navigation from '$lib/organisms/NavDark.svelte';
	import MobileNavigation from '$lib/organisms/MobileMenu.svelte';
</script>



<header>
<MobileNavigation></MobileNavigation>
<Navigation></Navigation>
</header>

<main>
<ContactForm></ContactForm>

<Location></Location>
</main>
<Footer></Footer>


<style>
    header{
    margin-bottom: 5rem;
}

 main{
    display:flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem 1.5rem;
    margin:2rem;
 }

</style>