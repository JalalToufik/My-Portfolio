<script>

</script>

<div class="hero-container">
    <div class="hero-title">
        <h1> 
            Front<span>end</span>
            Developer
        </h1>
        <p> Jalal Toufik</p>
        <div>
            <a class="btn-contact" href="/contact">Contact me</a>
        </div>
    </div>
</div>  

<style>

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
    h1, a{
        text-transform: uppercase;
    }
    h1, a{
        color: var(--accent-light-color);
    }
    h1{
        font-family: var(--hero-title-font);
        font-size: 2.5em;
        letter-spacing: .1em;
        line-height: 106%;
        max-width: 7em;
    }
    h1 span, .hero-title {
        color: var(--primary-color);
    }
    p, a{
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
    .hero-title p{
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

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        .hero-container{

            height: 90%;
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
            margin: 1em 0;
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

</style>