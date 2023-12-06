<script>
    import Carousel from "../../lib/atoms/Carousel.svelte";
    import SectionOneHome from "../../lib/organisms/SectionOneHome.svelte";
    import SectionTwoHome from "../../lib/organisms/SectionTwoHome.svelte";
    import SectionThreeHome from "../../lib/organisms/SectionThreeHome.svelte";
    import SectionFourHome from "../../lib/organisms/SectionFourHome.svelte";
    import SectionBannerHome from "../../lib/organisms/SectionBannerHome.svelte";
    export let data
</script>

<!--HTML -->

<!-- <Header data={data} /> -->
<Carousel/>

<main>
    <SectionOneHome/>
    <SectionTwoHome/>
    <SectionThreeHome/>
    <SectionFourHome data={data}  />
    <SectionBannerHome />
</main>

<!--CSS STYLING-->
<style>

    main {
        background-color: var(--background-color);

    }

</style>
