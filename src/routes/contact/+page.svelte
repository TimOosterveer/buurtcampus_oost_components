<script>
    import ContactForm from '$lib/molecules/ContactForm.svelte'
    import Location from '$lib/atoms/Location.svelte'
    import ContactInfo from '$lib/atoms/contactInfo.svelte'
    import Footer from '$lib/organisms/Footer.svelte'
    import Navigation from '$lib/organisms/NavDark.svelte'
	import MobileNavigation from '$lib/organisms/MobileMenu.svelte'

</script>

<header>
<MobileNavigation></MobileNavigation>
<Navigation></Navigation>
</header>

<main>
<section>
<ContactInfo></ContactInfo>
<ContactForm></ContactForm>
</section>
<Location></Location>

</main>

<Footer></Footer>


<style>
    header{
    margin-bottom: 5rem;
}

 main{
    margin:var(--margin);
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 2rem;
    justify-content: center;
 }



</style>