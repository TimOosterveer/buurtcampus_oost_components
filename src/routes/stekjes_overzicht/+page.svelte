<script>
    import StekjeCard from '$lib/atoms/StekjesCard.svelte'
    import Header from '$lib/organisms/Header.svelte'
    export let data
</script>


<Header></Header>

<!-- hier komt nog tekst -->
<main>
{#each data.stekjes as stekje}
<StekjeCard data={data}></StekjeCard>
{/each}
</main>

<!-- footer -->

<style>

 main{
    display:flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 1rem 1.5rem;
 }
</style>