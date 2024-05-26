<script>

</script>

<section id="About" class="about">
    <article>
        <h2>About me</h2>
        <p>
            I'm Jalal Toufik, a passionate frontend developer on the verge of graduating from Hogeschool van Amsterdam (HvA) with a degree in FDND - Frontend development.
        <p/>
        <p>
            During my studies, I've developed a strong foundation in HTML, CSS, and JavaScript, honing my skills through hands-on projects and coursework.
        </p>
    </article>
</section>

<style>
 /* ======= Article ======= */
    .about{
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 3em 2fr 3em;;
        grid-template-areas: "item1 title item2";
    }
    .about::before, .about::after {
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
        width: 1.5em;
    }
    article::before{    
        bottom: 14em;
        left: 0;
    }
    article::after{    
        left: 0;
    }
    .about::before{
        grid-area: item1;
    }
    .about::after{
        grid-area: item2;
    }
    .about article{
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
        .about{
            padding: 0 1.5em;
        }
        .about article{
            padding: 2em;
        }
        article::before, article::after{
            width: 3em;
        }
    }
</style>