<script>
	import { Navigation, HeroHeader, AboutMe, SkillBar, Projects } from '$lib/index';
</script>

<header>
    <Navigation />
    <HeroHeader />
    <SkillBar />
</header>



<main>
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
        height: 70vh;
        background-position-x: 55%;
        background-position-y: -55px;
    }

</style>