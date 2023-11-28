<script>
    import StekjeCard from '$lib/atoms/StekjesCard.svelte'
    import Header from '$lib/organisms/Header.svelte'
     import Footer from '$lib/organisms/Footer.svelte'
    export let data
</script>


<Header></Header>

<!-- hier komt nog tekst -->
<main>
{#each data.stekjes as stekje}
<StekjeCard data={data}></StekjeCard>
{/each}
</main>

<Footer></Footer>
<style>

 main{
    display:flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 1rem 1.5rem;
    margin-bottom: 5rem;
 }
</style>