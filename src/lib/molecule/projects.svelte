<script>
    import { onMount } from "svelte";
    import { writable } from "svelte/store";

   // GitHub API variables
    const username = "JalalToufik";
    const apiUrl = `https://api.github.com/users/${username}/repos?sort=updated&per_page=50`;

    // Store for repositories
    const repos = writable([]);

    /**
     * @param {any[]} repos An array of repository objects.
     */
    function filterRepos(repos) {
        const specificRepos = [ "ink-web-app","todo-app","spelen-met-css"];
        return repos.filter(repo => specificRepos.includes(repo.name.toLowerCase()));
    }
        
    onMount(async () => {
    try {
        const response = await fetch(apiUrl);
        let data = await response.json();

        const filteredRepos = filterRepos(data);
        // @ts-ignore
        repos.set(filteredRepos.sort((a, b) => {
            const order = [ "ink-web-app","todo-app","oba-web-app"];
            return order.indexOf(a.name.toLowerCase()) - order.indexOf(b.name.toLowerCase());
        }));
        } catch (error) {
        console.error("Error fetching repos:", error);
        }
    });
</script>

<section id="Projects">
    <h2>Projects</h2>

    <ul>
        {#each $repos as repo}
            <li data-index="0">
                <h3>
                    {#if repo}
                        {repo.name}
                    {/if}
                </h3>
                <p>
                    {#if repo}
                        {repo.description || "No description available."}
                    {/if}
                </p>
                <div>
                    <a href={repo.html_url} target="_blank">GitHub</a>
                    {#if repo.homepage}
                        <span>|</span>
                        <a href={repo.homepage} target="_blank">Website</a>
                    {/if}
                </div>
            </li>
        {/each}
    </ul>
</section>


<style>
    section {
        background-color: var(--secondary-color);
        width: 100%;
        display: grid;
        justify-items: center;
        align-items: center;
        grid-template-columns: 2fr 2fr;
        min-height: 90vh;
    }
    section h2 {
        color: var(--accent-light-color);
        transform: rotate(90deg);
        display: inline-block;
        font-size: 5em;
    }
    ul {
        color: var(--accent-light-color);
        padding: 2em 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-end;
    }
    li {
        width: 100%;
        padding: 1em 0;
        border-bottom: solid 2px var(--accent-light-color);
    }

    li:nth-last-of-type(3){
        padding: 0 0 1em 0;
    }

    li div{
        font-size: .8em;
        text-transform: uppercase;
        padding: .6em 0 0;
    }

    li a{
        color: var(--primary-color);
    }

    h3{
        font-family: var(--header-font);
        font-size: 1.8em;
        letter-spacing: 1.1px;
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        section h2 {
            font-size: 5.5em;
        }
        h3{
            font-size: 2.5em;
        }
    }

    /* MEDIA QUERY TABLET = 1250px */
    @media (min-width: 78.1rem) {
        section {
            grid-template-columns: 2fr 1.8fr;
        }
        section h2 {
            font-size: 7em;
        }
    }
</style>
