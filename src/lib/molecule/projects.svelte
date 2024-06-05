<script>

</script>

<section id="Projects">
    <h2>Projects</h2>

    <ul>
        <li>Project 1</li>
        <li>Project 2</li>
        <li>Project 3</li>
        <li>Project 4</li>
    </ul>
</section>

<style>
    section{
        background-color: var(--secondary-color);
        width: 100%;
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 2fr 2fr;
        height: 60vh;
    }
    section h2{
        color: var(--accent-light-color);
        transform: rotate(90deg);
        display: inline-block;
        font-size: 5em;
    }
    ul{
        color: var(--accent-light-color);
        padding: 2em 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-end;
    }
    li{
        width: 100%;
        padding: 1em 0;
        border-bottom: solid 2px var(--accent-light-color);
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        section h2 {
            font-size: 5.5em;
        }
    }


    /* MEDIA QUERY TABLET = 1250px */
    @media (min-width: 78.1rem) {
        section{
            grid-template-columns: 2fr 1.8fr;
        }
        section h2{
            font-size: 6em;
        }

    }

</style>