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

<style>
    nav{
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        padding: 0 1em;
    }
    nav ul{
        display: flex;
        padding: .5em;
        gap: 1em;
        font-size: 1em;
    }
    nav a{
        color: var(--accent-light-color);
        font-family: var(--hero-title-font);
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
        height: .1em;
    }
    .border-1, .border-2{
        background-color: #e5dfd352;
        height: .1em;
    }
    .border-1{
        width: 1.5em;
    }
    .border-2{
        width: 95%;
    }
    h1{
        font-family: var(--logo-font);
        font-size: 2em;
        color: var(--primary-color);
        margin: 0 .3em;
        position: relative;
        bottom: 0.8em;
        text-transform: uppercase;
    }
    h1 span{
        color: var(--accent-light-color);
    }

    /* MEDIA QUERY MOBILE = 400px */
    @media (min-width: 25rem) {

    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        nav ul{
                gap: 2.5em;
                padding: 1em;
            }
        h1{
            font-size: 2.5em;
        }
    }
</style>