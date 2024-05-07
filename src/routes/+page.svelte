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
        padding: 0 1em;
    }
    nav ul{
        display: flex;
        padding: 1.2em;
        gap: 4em;
        font-size: 14px;
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
        padding: 0 .5em;
    }
    .border-1, .border-2{
        background-color: #e5dfd352;
        height: .35em;
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
        font-family: var(--logo-font);
        font-size: 3.5em ;
        margin: 0 .3em;
        position: relative;
        bottom: 0.8em;
    }
    h1, h2, a,  .skill-bar ul{
        text-transform: uppercase;
    }
    h1, h2, a{
        color: var(--accent-light-color);
    }
    h2{
        font-family: var(--hero-title-font);
        font-size: 7.5em;
        width: 6em;
        letter-spacing: .1em;
        line-height: 106%;
        text-align: right;
    }
    h1 span, h2 span, .hero-title a{
        color: var(--primary-color);
    }
    h3, a, .skill-bar ul{
        letter-spacing: .1em;
    } 
    h3{
        font-size: 1.3em;
        color: var(--accent-light-color);
        font-family: var(--header-font);
        letter-spacing: .5em;
        padding: 1em 0;
    }
    .hero-title a{
        margin: .5em;
        padding: 0.2em 2em;
        font-size: 14px;
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