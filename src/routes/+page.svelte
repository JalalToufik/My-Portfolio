<div class="hero-bg">
    <header>
        <nav>
            <ul>
                <li><a href="/about">About</a></li>
                <li><a href="/projects">Projects</a></li>
                <li><a href="/contact">Contact</a></li>
            </ul>
            <div class="nav-border">
                <div class="border-1"></div>
                <h1><span>J</span>T</h1>
                <div class="border-2"></div>
            </div>
        </nav>
    </header>

    <section class="hero-title">
        <h2> <span>J</span>alal Toufik</h2>
        <h3> Frontend Developer </h3>
        <a href="/contact">Contact me</a>
    </section>  
</div>

<div class="skill-bar">
    <ul>
        <li>// CSS //</li>
        <li>// HTML //</li>
        <li>// Javascript //</li>
    </ul>
</div>


<style>
    .hero-bg{
        background-image: url(/jalal.png);
        background-repeat: no-repeat;
        background-position: top left;
        background-size: cover;
        width: 100%;
        height: 80vh;
    }
    nav{
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        padding: 1em;
    }
    nav ul{
        display: flex;
        padding: 1em;
        gap: 3em;
    }
    nav a{
        color: white;
        font-family: var(--header-font);
    }
    nav a:active{
        color: var(--accent-color);
    }
    nav a:hover{
        color: var(--primary-color);
    }
    .nav-border{
        width: 100%;
        display: flex;
    }
    .border-1, .border-2{
        background-color: #a7a599a9;
        height: .5em;
        border-radius: 1em;
    }
    .border-1{
        width: 5%;
    }
    .border-2{
        width: 95%;
    }
    .hero-title{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        padding: 1em 5em;
    }
    h1{
        font-size: 3em ;
        margin: 0 .5em;
        position: relative;
        bottom: 0.7em;
    }
    h1, h2, a,  .skill-bar ul{
        text-transform: uppercase;
    }
    h1, h2{
        font-family: var(--hero-title-font);
        color: var(--accent-light-color);
    }
    h2{
        font-size: 7em;
        width: 6em;
        letter-spacing: 4px;
        line-height: 106%;
        text-align: right;
    }
    h1 span, h2 span, .hero-title a{
        color: var(--primary-color);
    }

    h3{
        color: var(--accent-light-color);
        font-family: var(--header-font);
        letter-spacing: .5em;
        padding: 1em 0;
    }
    .hero-title a{
        margin: 0 .5em;
        padding: 0.2em 1.5em;
        border: solid 2px var(--primary-color);
    }
    .hero-title a:hover{
        color: white;
        border-color: white;
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

    .skill-bar ul{
        display: flex;
        justify-content: space-around;
        width: 100%;
    }


</style>