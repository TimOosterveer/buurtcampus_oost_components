<script>
    import StekjeCard from '$lib/atoms/StekjesCard.svelte'
    export let data
</script>

{#each data.stekjes as stekje}
<StekjeCard data={data}></StekjeCard>
{/each}