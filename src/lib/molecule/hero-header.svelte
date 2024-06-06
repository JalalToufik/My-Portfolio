<script>

</script>

<div class="hero-container">
    <div class="hero-title">
        <h1> 
            <span>Let's</span> Craft the Reality You Envision
        </h1>
        <h2>Your Vision, My Expertise</h2>
        <p> Jalal Toufik | <span>Frontend Developer</span></p>
        <div>
            <a class="btn-contact" href="#Contact">Contact me</a>
        </div>
    </div>
</div>  

<style>
    .hero-container{
        display: flex;
        min-height: 80vh;
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
    h1, a{
        text-transform: uppercase;
    }
    h1, a{
        color: var(--accent-light-color);
    }
    h1{
        font-family: var(--hero-font);
        font-size: 2.5em;
        line-height: 106%;
        max-width: 10em;
    }
    h2, p span {
        color: var(--primary-color);
    }

    h2{
        font-size: 2em;
        margin: 0 .2em ;
        letter-spacing: 5px;
        font-family:var(--hero-title-font) ;
    }
    p, a{
        letter-spacing: .1em;
    } 
    .hero-title div{
        position: absolute;
        top: 4em;
        right: 2em;
        display: flex;
        align-items: start;
        padding: 1em 0;
    }
    .hero-title p{
        font-size: 1.2em;
        color: var(--accent-light-color);
        font-family: var(--hero-title-font);
        text-transform: uppercase;
        padding: 4em 0 0 0;
    }
    .btn-contact{
        width: 7.5em;
        padding: 0.2em .5em;
        font-size: 18px;
        z-index: 0;
        letter-spacing: -1px;
        border-radius: 2em;
        border: solid 2px var(--accent-light-color);
        color: var(--accent-light-color);
        transition: ease-out .3s;
    }
    .btn-contact:hover{
        color: var(--primary-color);
        border-color: var(--primary-color);
        transform: scale(1.03);
    }

    /* MEDIA QUERY MOBILE = 400px */
    @media (min-width: 25rem) {
        h1{
            font-size: 3.5em;
        }
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        .hero-container{
            padding: 6em;
        }
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
        h1{
            grid-area: title;
            font-size: 4.5em;
            margin: .5em 0;
        }
        h2{
            grid-area: title;
        }
        .hero-title p{
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

    /* MEDIA QUERY TABLET = 1250px */
    @media (min-width: 78.1rem) {

        h1{
            font-size: 5.5em;
        }
    }

</style>