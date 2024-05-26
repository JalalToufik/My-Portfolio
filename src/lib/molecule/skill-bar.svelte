<script>

</script>

<section class="skill-bar">
    <!-- svelte-ignore a11y-distracting-elements -->
    <marquee>
        <span>// Css // </span>
        <span>// Html // </span>
        <span>// Javascript // </span>
        <span>// Responsive Websites // </span>
        <span>// Accessible Websites // </span>
        <span>// Progressive enhancement // </span>
        <span>// Performance // </span>
    </marquee>
</section>

<style>
    .skill-bar{
        background-color: var(--secondary-color);
        width: 100%;
        height: 2em;
        color: white;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    marquee{
        text-transform: uppercase;
        animation: 5s linear infinite;
    }
    marquee span{
        padding: 0 4em;
    }
</style>