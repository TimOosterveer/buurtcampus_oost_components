<script>
  export let data;

  import Header from '$lib/molecules/HeaderImage.svelte'
  import Info from '$lib/organisms/InfoWorkshop.svelte'
  import Card from '$lib/organisms/OverviewWorkshops.svelte'
  import Footer from '../../lib/organisms/Footer.svelte';
  import NavDark from '../../lib/organisms/NavDark.svelte';
  import MobileMenu from '../../lib/organisms/MobileMenu.svelte';
</script>

<NavDark />
<MobileMenu />

<Header data={data}/>
<Info/>
<Card data={data}/>

<Footer />
