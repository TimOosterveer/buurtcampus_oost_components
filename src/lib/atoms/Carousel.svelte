<script>
    import {onDestroy, onMount} from 'svelte';
    import image1 from '$lib/assets/carousel-img-1.jpg'
    import image2 from '$lib/assets/carousel-img-2.jpg'
    import image3 from '$lib/assets/carousel-img-3.jpg'
    import ButtonGelijkSwappen from "./ButtonGelijkSwappen.svelte";


    let intervalId;

    onMount(() => {
        const carrouselContainer = document.querySelector('.carrousel');
        const carrousel = document.querySelector('.carrousel-a');

        const interval = 8000;

        intervalId = setInterval(() => {

            const currentScroll = carrousel.scrollLeft;
            const itemWidth = carrouselContainer.clientWidth;
            const totalWidth = carrousel.scrollWidth;

            const nextScroll = (currentScroll + itemWidth) % totalWidth;

            carrousel.scrollTo({
                left: nextScroll,
                behavior: 'smooth'
            });
        }, interval);
    });

    onDestroy(() => {

        clearInterval(intervalId);
    });
</script>

<main>
<div class="carrousel" aria-label="Carousel">
    <h1>Swap nu je stekjes!</h1>
    <ButtonGelijkSwappen/>
    <div class="carrousel-a">
        <div class="carrousel-picture"><img src={image1} alt="Slide 1"
                                            aria-label="carousel-image-1"></div>
        <div class="carrousel-picture"><img src={image2} loading=”lazy” alt="Slide 2"
                                            aria-label="carousel-image-2"></div>
        <div class="carrousel-picture"><img src={image3} loading=”lazy” alt="Slide 3"
                                            aria-label="carousel-image-3"></div>

    </div>

</div>
</main>

<style>

    main {
        background-color: var(--background-color);
    }

    .carrousel {
        width: 100%;
    }

    .carrousel h1 {
        position: absolute;
        z-index: 1;
        width: 60%;
        color: var(--text-color);
        display: flex;
        text-align: center;
        justify-content: center;
        align-items: center;
        height: 35%;
        left: 20%;
    }

    .carrousel img {
        width: 100%;
        height: auto;
        aspect-ratio: 16 / 9;
        object-fit: cover;
    }

    .carrousel-a {
        display: flex;
        overflow: auto;
        scroll-snap-type: x mandatory;
        scrollbar-width: none;
    }

    .carrousel-a::-webkit-scrollbar {
        display: none;
    }

    .carrousel-picture {
        flex-grow: 0;
        flex-shrink: 0;
        flex-basis: 100%;
        scroll-snap-align: center;
    }

    /* MEDIA QUERY TABLET*/
    @media screen and (min-width: 48rem) {

        .carrousel h1 {
            width: 50%;
            height: 45%;
            left: 25%;
            font-size: 3rem;
        }
    }

    /* MEDIA QUERY DESKTOP */
    @media screen and (min-width: 64rem) {
        .carrousel h1 {
            width: 25rem;
            height: 100%;
            left: 38%;
            font-size: 5rem;
            line-height: 7rem;
        }
    }
</style>