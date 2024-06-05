<script>

</script>

<section>
    <form>
        <fieldset>
            <legend id="Contact">Contact me</legend>

            <label for="name">Name</label>
            <input id="name" required type="text">

            <label for="mail" >E-mail</label>
            <input id="mail" type="email" required>  

            <label for="message">Message</label>
            <textarea id="message" name="message" rows="3" cols="33"></textarea>

            <button>Send</button>
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
        grid-template-columns: 1fr 1fr;
        grid-template-areas: "title form";
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
        gap: 2.5em;
    }

    h2{
        width: 3em;
        font-size: 6em;
        height: 3em;
        line-height: 90%;
    }

    h2 span{
        color: var(--primary-color);
    }

    p, legend{
        text-transform: uppercase;
        font-family: var(--header-font);
        font-size: 2.5em;
    }

    legend{
        padding-bottom: .5em;
    }

    form{
        display: flex;
        justify-content: center;
        width: 100%;
        align-items: flex-start;
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
        padding: .5em;
    }


</style>