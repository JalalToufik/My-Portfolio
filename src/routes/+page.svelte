<script>
	import { Navigation, HeroHeader, AboutMe, SkillBar, Projects } from '$lib/index';
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


<style>
    header{
        background-attachment: fixed;
        background-image: url(/jalal.png);
        background-size: cover;
        background-color: rgb(51, 51, 51);
        background-repeat: no-repeat;
        height: 65vh;
        background-position-x: 35%;
        background-position-y: -55px;
    }

</style>