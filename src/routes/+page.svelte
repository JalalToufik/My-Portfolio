<script>
	import { Header } from '../lib/index';
</script>

<div class="hero-bg">

    <Header />

    <section class="hero-container">
        <div class="hero-title">
            <h2> 
                Front<span>end</span>
                Developer
            </h2>
            <h3> Jalal Toufik</h3>
            <div>
                <a class="btn-contact" href="/contact">Contact me</a>
            </div>
        </div>
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
        background-color: black;
        background-repeat: no-repeat;
        height: 70vh;
        background-position-x: 50%;
        background-size: cover;
    }

    .hero-container{
        display: flex;
        flex-direction: column-reverse;
        justify-content: space-between;
        height: 95%;
        padding: 3em;
    }

    .hero-title{
        display: flex;
        justify-content: flex-end;
        align-items: start;
    }
    .hero-title{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }
    h2, a,  .skill-bar ul{
        text-transform: uppercase;
    }
    h2, a{
        color: var(--accent-light-color);
    }
    h2{
        font-family: var(--hero-title-font);
        font-size: 2.5em;
        letter-spacing: .1em;
        line-height: 106%;
        max-width: 7em;
    }
    h2 span, .hero-title {
        color: var(--primary-color);
    }
    h3, a, .skill-bar ul{
        letter-spacing: .1em;
    } 
    .hero-title div{
        position: absolute;
        top: 4em;
        right: 2em;
        display: flex;
        justify-content: flex-end;
        align-items: start;
        padding: 1em 0;
    }
    h3{
        font-size: 1.3em;
        color: var(--accent-light-color);
        font-family: var(--hero-title-font);
        text-transform: uppercase;
        padding: 1em 0 0 0;
    }
    .btn-contact{
        width: 7.5em;
        padding: 0.2em .5em;
        font-size: 18px;
        letter-spacing: -1px;
        border-radius: 2em;
        border: solid 2px var(--accent-light-color);
        color: var(--accent-light-color);
    }
    .btn-contact:hover{
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

    /* MEDIA QUERY MOBILE = 400px */
    @media (min-width: 25rem) {

    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        /* .hero-container{
            padding: 4em;
            justify-content: flex-start;
            align-items: start;
            height: 90%;
        }
        .hero-title div{
            top: 31em;
            left: 4em;
            justify-content: flex-start;
        }
        */

        .hero-title{
            display: grid;
            justify-content: start;
            align-items: end;
            grid-template-columns: 2fr 1fr;
            grid-template-rows: 3fr 1fr;
            grid-template-areas:
            'title title'
            'button myName';
        }
        h2{
            grid-area: title;
            font-size: 4.5em;
            margin: 1em 0;
        }
        h3{
            grid-area: myName;
            text-align: right;
            padding: 0;
        }

        .hero-title div{
            grid-area: button;
            position:static;
            justify-content: flex-start;
            padding: 0;
        }

    }


</style>