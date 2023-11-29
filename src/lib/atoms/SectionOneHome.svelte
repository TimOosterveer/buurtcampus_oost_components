<script>
    import ButtonLocation from "./ButtonLocation.svelte";
</script>

<html>

<div class="container-text-one">
    <h2>Doe mee!</h2>
    <p>Heb jij een of meerdere plantenstekjes over en zou je die graag willen ruilen voor een nieuw plantje? Meld je
        stekje
        hier aan en ruil ‘m via de app. Schrijf de Latijnse naam van je plant en eventuele verzorgingstips op een
        labeltje
        en neem ‘m mee naar de OBA Linnaeusstraat in Amsterdam.</p>
</div>

<ButtonLocation/>

</html>


<style>
    h2 {
        color: var(--text-color);
        margin-bottom: 1rem;
    }

    p {
        color: var(--text-color);
    }

    .container-text-one {
        padding-top: 3rem;
        padding-bottom: 3rem;
        padding-left: 2rem;
        width: 95%;
    }



    /* MEDIA TABLET*/
    @media screen and (min-width: 48rem) {

        h2 {
            font-size: 3rem;
        }

        .container-text-one {
            padding-left: 6rem;
            width: 80%;
        }
    }

    /* MEDIA QUERY DESKTOP */
    @media screen and (min-width: 64rem) {
        h2 {
            font-size: 5rem;
        }

        p {
            font-size: 1.3rem;
        }

        .container-text-one {
            padding-left: 30rem;
            width: 75%;
        }
    }
</style>