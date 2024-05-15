<script>
	import { Header } from '../lib/index';
</script>

<div class="hero-bg">

    <Header />

    <div class="hero-container">
        <section class="hero-title">
            <h2> Front<span>end</span></h2>
            <h2> Developer</h2>
            <div>
                <h3> Jalal Toufik</h3>
            </div>
        </section>  
        <div>
            <a class="btn-contact" href="/contact">Contact me</a>
        </div>
    </div>  
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
        height: 80%;
        padding: 2em;
    }

    .hero-container div{
        display: flex;
        justify-content: flex-end;
    }
    .hero-title{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding: 1em;
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
        width: 6em;
        letter-spacing: .1em;
        line-height: 106%;
        text-align: right;
    }
    h2 span, .hero-title {
        color: var(--primary-color);
    }
    h3, a, .skill-bar ul{
        letter-spacing: .1em;
    } 
    .hero-title div{
        display: flex;
        width: 100%;
        justify-content: flex-start;
        padding: 1em 0;
    }
    h3{
        font-size: .8em;
        color: var(--accent-light-color);
        font-family: var(--hero-title-font);
        text-transform: uppercase;
    }
    .btn-contact{
        width: 10em;
        padding: 0.2em 1em;
        font-size: 14px;
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


</style>