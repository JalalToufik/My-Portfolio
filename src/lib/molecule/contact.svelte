<script>

</script>

<section>
    <form action="https://api.web3forms.com/submit" method="POST">
        <input type="hidden" name="access_key" value="25decdef-5f8c-436d-bbf1-9c2af8bda1e4">
        <fieldset>
            <legend id="Contact">Contact me</legend>

            <label for="name">Name</label>
            <input id="name" required type="text">

            <label for="mail" >E-mail</label>
            <input id="mail" type="email" required>  

            <label for="message">Message</label>
            <textarea id="message" name="message" rows="3" cols="33"></textarea>

            <button type="submit">Send</button>
        </fieldset>
    </form>
    <article>
        <h2>Lets inovate <span>together</span></h2>
        <p>mj.toufik@hotmail.com</p>
    </article>
</section>

<style>
    section{
        display: grid;
        grid-template-columns: 1fr;
        grid-template-areas: "title";
        position: relative;
        background-color: var(--secondary-color);
        border: 2px solid var(--accent-light-color);
        color: var(--accent-light-color);
        border-radius: 5px;
        padding: 2em;
        width: 88%;
    }

    article{
        grid-area: title;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    h2{
        width: 3em;
        font-size: 5.5em;
        height: 3em;
        line-height: 90%;
    }

    h2 span{
        color: var(--primary-color);
    }

    p, legend{
        text-transform: uppercase;
        font-family: var(--header-font);
        font-size: 2.2em;
    }

    legend{
        padding-bottom: .5em;
    }

    form{
        display: flex;
        justify-content: center;
        width: 100%;
        align-items: flex-start;
        padding: 2em 0;
    }

    fieldset{
        display: flex;
        text-transform: uppercase;
        flex-direction: column;
        border: none;
        gap: .5em;
        width: 50%;
    }

    form input, textarea{
        background-color: var(--accent-darkest-color);
        font-family: var(--label-font);
        border: none;
        color: white;
        padding: .5em;
    }

    form input:focus, textarea:focus{
        background-color: white;
        color: black;
    }

    textarea{
        resize: none;
    }
    form input:valid {
        border-color:white;
    }
    form input:invalid {
        border-color:red;
    }
    form:valid button {
        opacity:1
    }
    button:focus {
        transform: scale(1.1, 1.1);
    }
    button{
        padding: 0.2em .5em;
        z-index: 0;
        background-color: unset;
        letter-spacing: 5px;
        border-radius: 2em;
        border: solid 2px var(--primary-color);
        color: var(--primary-color);
        opacity:0;
        text-transform: uppercase;
        font-weight: bold;
    }
    button:hover{
        background-color:var(--accent-light-color);
        color: var(--secondary-color);
        border-color: var(--accent-light-color);
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        section{
            grid-template-columns: 1fr 1fr;
            grid-template-areas: "title form";
            padding: 6em 2em;
        }

        article{
            gap: 2.5em;
        }
        h2{
            font-size: 6em;
        }
        p, legend{
            font-size: 2.5em;
        }

        form{
            padding: unset;
        }
    }

</style>