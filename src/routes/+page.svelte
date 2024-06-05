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
        height: 75vh;
        background-position-x: 35%;
        background-position-y: -55px;
    }

    main{
        position: relative;
        z-index: 1;
    }

    footer{
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 5em 0;
        background-color: var(--accent-dark-color);
    }

    footer::before{
        content: "";
        border: 2px solid var(--accent-light-color);
        position: absolute;
        border-top: none;
        border-bottom: none;
        height: 71vh;
        width: 75%;
        margin: 0 auto;
    }

</style>