<script>
    import {onDestroy, onMount} from 'svelte';

    let intervalId;

    onMount(() => {
        const carrouselContainer = document.querySelector('.carrousel');
        const carrousel = document.querySelector('.carrousel-a');

        const interval = 4000;

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

<div class="carrousel" aria-label="Carousel">
    <div class="carrousel-a">
        <div class="carrousel-picture"><img src="src/lib/assets/carousel-img-1.jpg" alt="Slide 1"
                                            aria-label="carousel-image-1"></div>
        <div class="carrousel-picture"><img src="src/lib/assets/carousel-img-2.jpg" loading=”lazy” alt="Slide 2"
                                            aria-label="carousel-image-2"></div>
        <div class="carrousel-picture"><img src="src/lib/assets/carousel-img-3.jpg" loading=”lazy” alt="Slide 3"
                                            aria-label="carousel-image-3"></div>
    </div>
</div>

<style>
    .carrousel {
        width: 100%;
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

    .carrousel-a::-webkit-scrollbar { display: none; }

    .carrousel-picture {
        flex-grow: 0;
        flex-shrink: 0;
        flex-basis: 100%;
        scroll-snap-align: center;
    }
</style>