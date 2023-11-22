<script>
  import Header from "../../lib/molecules/Header.svelte";
  import Carousel from "../../lib/atoms/Carousel.svelte";
  export let data
</script>

<Header data={data} />
<Carousel/>
