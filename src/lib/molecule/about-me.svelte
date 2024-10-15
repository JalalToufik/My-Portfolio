<script>

</script>

<section id="About">
    <article>
        <h2>About me</h2>
        <p>
            Hi, I'm Jalal! As a frontend developer and designer, I combine my love for code with a passion for aesthetics. 
        <p/>
        <p>
            During my studies at the HvA, I've learned how to transform technical knowledge into beautiful, interactive web pages. Whether it's building a responsive website or animating complex UI elements, I love enhancing user experiences.
        </p>
    </article>
</section>

<style>
 /* ======= Article ======= */
    section{
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 21% 2fr 21%;
        grid-template-areas: "item1 title item2";
        min-height: 60vh;
    }
    section::before, section::after {
        content: "";
        border: 1px solid var(--secondary-color);
        height: 100%;
        position: relative;
        top: -.2em;
    }
    article::before, article::after{
        content: "";
        position: absolute;
        background-color: var(--secondary-color);
        height: 2px;
        width: 10.5%;
    }
    article::before{    
        top: 10.5em;
        left: 0;
    }
    article::after{    
        left: 0;
    }
    section::before{
        grid-area: item1;
    }
    section::after{
        grid-area: item2;
    }
    article{
        grid-area: title;
        padding: 1em;
        margin-bottom: 2em;
    }
    h2{
        border-bottom: 2px solid var(--secondary-color);
        margin-bottom: .5em;
    }
    p{
        max-width: 50em;
        text-transform: uppercase;
        padding: .2em 0;
    }

    /* MEDIA QUERY TABLET = 434px */
    @media (min-width: 27.2rem) {
        article::after{    
            right: 0;
            left: unset;
        }
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        section{
            padding: 0 1.5em;
        }
        article{
            padding: 2em;
        }
        article::before, article::after{
            width: 12.7%;
            max-width: 7.3em;
        }
        h2 {
            font-size: 5.5em;
        }
    }

    /* MEDIA QUERY TABLET = 972px */
    @media (min-width: 60.75rem) {
        article::before, article::after{
            width: 12.4%;
            max-width: 9.8em;
        }
    }

    /* MEDIA QUERY TABLET = 1250px */
    @media (min-width: 78.1rem) {
        h2{
            font-size: 6em;
        }
    }

    /* MEDIA QUERY TABLET = 1335px */
    @media (min-width: 83.43rem) {
        article::before, article::after{
            width: 11.7%;
            max-width: 13.8em;
        }
    }
</style>