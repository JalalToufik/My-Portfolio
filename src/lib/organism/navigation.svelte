<script>
	import { OpenMenu, CloseMenu } from '$lib/index.js';
    let navActive = false;

    const toggleNav = () => {
        navActive = !navActive;
    };
</script>

<section>
    <div class="nav-border">
        <a href="/" class="logo">J<span>T</span></a>
    </div>
    <!-- svelte-ignore a11y-invalid-attribute -->
    <a href="javascript:void(0)" class="menu-icon" on:click={toggleNav}>
        <img class="menu" src={navActive ? CloseMenu : OpenMenu} alt="Menu button"/>
    </a>
    <nav class:active={navActive}>
        <ul role="menu">
            <li><a href="#About" on:click={toggleNav}>//About</a></li>
            <li><a href="#Projects" on:click={toggleNav}>//Projects</a></li>
            <li><a href="#Contact" on:click={toggleNav}>//Contact</a></li>
        </ul>
    </nav>
</section>

<style>
    section{
        width: 100%;
    }
    nav{
        flex-direction: column;
        align-items: flex-end;
        background-color: var(--secondary-color);
        padding: 0 1em;
        visibility: hidden;
        transform: translateY(-100%);
        opacity: 0;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        transition: transform 0.25s ease-in-out, opacity 0.25s ease-in-out;
        z-index: 99;
    }
    nav.active {
        visibility: visible;
        transform: translateY(0);
        opacity: 1;
        transition: transform 0.25s ease-in-out, opacity 0.25s ease-in-out visibility 0s linear 0.5s;
	}

    nav ul{
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 2em;
        padding: 5em 0;
        font-size: 2em;
    }

    nav li{
        width: 80%;
        border-bottom: 2px solid white;
    }

    nav li:hover{
        border-color: var(--primary-color);
    }

    nav li:hover a{
        color: var(--primary-color);
    }

    .menu{
        background: none;
        transform: rotate(180deg);
        padding: 1em;
        position: absolute;
        top: 0;
        right: 0;
        z-index: 100;
    }
    nav a{
        color: var(--accent-light-color);
        font-family: var(--hero-title-font);
    }
    nav a:active{
        color: var(--accent-color);
    }

    .nav-border{
        width: 100%;
        display: flex;
        padding: 0 1em;
        height: .1em;
        z-index: 99;
        position: absolute;
        top: 3em;
        left: 0;
    }
    .nav-border::before, .nav-border::after{
        background-color: #e5dfd352;
        height: .15em;
    }
    .nav-border::before{
        content: "";
        width: 2em;
    }
    .nav-border::after{
        content: "";
        width: 95%;
    }
    .logo{
        height: 1.7em;
        font-family: var(--logo-font);
        font-size: 2em;
        color: var(--primary-color);
        margin: 0 .3em;
        position: relative;
        bottom: 0.8em;
        text-transform: uppercase;
        letter-spacing: -4px;
        z-index: 99;
    }

    .logo:hover {
		cursor: pointer;
        transform: scale(1.1);
	}
    .logo span{
        color: var(--accent-light-color);
    }

    @media (min-width: 56.25em) {

        .menu {
            display: none;
        }
        nav {
            display: flex;
            background: none;
            padding: .7em 2.5em;
            width: 100%;
            height: unset;
            opacity: 1;
            visibility: visible;
            transform: none;
        }

        nav ul{
            font-size: 1em;
            flex-direction: row;
            padding: 0;
        }
        nav li{
            width: inset;
            border-bottom: none;
        }
        .nav-border{
            padding: 0 2.5em;
        }
        .nav-border::before{
            width: 3.5em;
        }
        .nav-border::after{
            content: "";
            width: 100%;
        }
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {

        .logo{
            font-size: 2.5em;
        }
    }

    /* MEDIA QUERY TABLET = 1250px */
    @media (min-width: 78.1rem) {
        .nav-border{
            top: 3.2em;
        }

        nav ul{
            font-size: 1.1em;
        }
    }

</style>