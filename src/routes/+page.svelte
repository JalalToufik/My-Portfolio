<script>
	import { Navigation, HeroHeader, AboutMe, SkillBar, Projects, Contact } from '$lib/index';
</script>

<header>
    <Navigation />
    <HeroHeader />
</header>

<main>
    <SkillBar />
    <AboutMe />
    <Projects />
</main>

<footer>
    <Contact />
</footer>

<style>
    header{
        background-attachment: fixed;
        background-image: url(/jalal.png);
        background-size: cover;
        background-color: rgb(51, 51, 51);
        background-repeat: no-repeat;
        min-height: 79vh;
        background-position-x: 35%;
        background-position-y: -55px;
    }

    main{
        position: relative;
        z-index: 1;
    }

    footer{
        position: relative;
        z-index: 1;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        padding: 5em 0;
        background-color: var(--accent-dark-color);
    }

    footer::before{
        content: "";
        border: 2px solid var(--accent-light-color);
        position: absolute;
        border-top: none;
        border-bottom: none;
        height: 100%;
        width: 75%;
        margin: 0 auto;
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        footer{
            height: unset;
        }

    }

</style>