<script>
	import { Navigation, HeroHeader } from '$lib/index';
</script>

<header>
    <Navigation />
    <HeroHeader />
</header>

<section class="skill-bar">
    <!-- svelte-ignore a11y-distracting-elements -->
    <marquee>
        <span>// Css // </span>
        <span>// Html // </span>
        <span>// Javascript // </span>
        <span>// Responsive Websites // </span>
        <span>// Accessible Websites // </span>
        <span>// Progressive enhancement // </span>
        <span>// Performance // </span>
    </marquee>

</section>

<main>
    <section class="about">
        <div class="grid-item"></div>
        <h2>About me</h2>
        <p>
            I'm Jalal Toufik, a passionate frontend developer on the verge of graduating from Hogeschool van Amsterdam (HvA) with a degree in [FDND - Frontend development].
            During my studies, I've developed a strong foundation in HTML, CSS, and JavaScript, honing my skills through hands-on projects and coursework.
        </p>
        <div class="grid-item2"></div>
    </section>

    <section class="projects">
        <h2>Projects</h2>
    </section>
</main>


<style>
    header{
        background-attachment: fixed;
        background-image: url(/jalal.png);
        background-size: cover;
        background-color: rgb(51, 51, 51);
        background-repeat: no-repeat;
        height: 70vh;
        background-position-x: 55%;
        background-position-y: -55px;
    }
    .skill-bar{
        background-color: var(--secondary-color);
        width: 100%;
        height: 2em;
        color: white;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    marquee{
        text-transform: uppercase;
        animation: 5s linear infinite;
    }

    marquee span{
        padding: 0 4em;
    }

    h2{
        font-size: 4.5em;
        text-transform: uppercase;
        font-family: "League Gothic", sans-serif;
    }

    .about h2{
        grid-area: title;
    }

    .about{
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 3em 2fr 3em ;
        grid-template-rows: 40% 2fr 10em;
        grid-template-areas:
        "item1 title item2"
        ".... paragraph .... "
    }

    .about::before, .about::after {
        content: "";
        border: 2px solid var(--secondary-color);
        height: 100%;
        position: relative;
        top: -.2em;
    }
    .about::before{
        grid-area: item1;
    }
    .about::after{
        grid-area: item2;
    }
    p{
        grid-area: paragraph;
        padding-top: 2em;
        max-width: 32em;
        border-top: 4px solid var(--secondary-color);
        text-transform: uppercase;
    }

    .projects{
        background-color: var(--secondary-color);
        width: 100%;
        height: 30em;
        padding: 10em 2em;
        display: flex;
        align-items: flex-start;
    }

    .projects h2{
        color: var(--accent-light-color);
        transform: rotate(90deg);
        display: inline-block;
    }
</style>