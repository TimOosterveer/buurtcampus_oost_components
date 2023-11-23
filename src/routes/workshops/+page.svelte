<script>
  export let data;
  import Info from '$lib/organisms/InfoWorkshop.svelte'
  import Card from '$lib/organisms/OverviewWorkshops.svelte'
</script>

<Info/>
<Card data={data}/>