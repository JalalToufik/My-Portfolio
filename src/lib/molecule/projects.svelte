<script>
    import { onMount } from "svelte";
    import { writable } from "svelte/store";

    // GitHub API variables
    const username = "JalalToufik";
    const apiUrl = `https://api.github.com/users/${username}/repos?sort=updated&per_page=50`;

    // Store for repositories
    let repos = writable([]);

    // Function to filter repositories based on specific names
    function filterRepos(repos) {
        const specificRepos = [
            "bieb-in-bloei",
            "ink-web-app",
            "oba-web-app"
        ];
        return repos.filter(repo => specificRepos.includes(repo.name.toLowerCase()));
    }

    onMount(async () => {
        // Fetch and set repositories
        try {
            const response = await fetch(apiUrl);
            if (!response.ok) {
                throw new Error(`Error fetching repos: ${response.statusText}`);
            }
            let data = await response.json();
            // Sort repositories by stargazers count in descending order and then reverse the order
            data.sort((a, b) => b.stargazers_count - a.stargazers_count);
            data.reverse();
            repos.set(filterRepos(data));
        } catch (error) {
            console.error("Error fetching repos:", error);
            // You can display an error message to the user here
        }
    });
</script>

<section id="Projects">
    <h2>Projects</h2>

    <ul>
        {#each $repos as repo}
            <li data-index="0">
                <h3 class="card-title">
                    {#if repo}
                        {repo.name}
                    {/if}
                </h3>
                <p class="card-description">
                    {#if repo}
                        {repo.description || "No description available."}
                    {/if}
                </p>
                <div>
                    <a href={repo.html_url} target="_blank"> GitHub</a>
                    <span>|</span>
                    <a href={repo.homepage} target="_blank"> Website </a>
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
        min-height: 80vh;
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

    li:nth-last-of-type(1){
        padding: 0 0 1em 0;
    }

    li a{
        color: var(--primary-color);
    }

    /* MEDIA QUERY TABLET = 768px */
    @media (min-width: 48rem) {
        section h2 {
            font-size: 5.5em;
        }
    }

    /* MEDIA QUERY TABLET = 1250px */
    @media (min-width: 78.1rem) {
        section {
            grid-template-columns: 2fr 1.8fr;
        }
        section h2 {
            font-size: 6em;
        }
    }
</style>
