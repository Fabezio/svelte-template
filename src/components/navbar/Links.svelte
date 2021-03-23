<script>
    export let segment;
    console.log(typeof segment);
    const localLinks = [
        { url: undefined, label: "Accueil" },
        { url: "about", label: "A propos" },
        { url: "blog", label: "Le blog", hasRel: true },
        { url: "infos", label: "Infos", hasRel: true },
        // { url: "files", label: "Fichiers" },
    ];
    console.table(localLinks);
</script>

<ul>
    {#each localLinks as link}
        <li>
            {#if !link.hasRel}
                <a
                    aria-current={segment === link.url ? "page" : undefined}
                    href={link.url == undefined ? "." : link.url}
                    >{link.label}</a
                >
            {:else}
                <a
                    rel="prefetch"
                    aria-current={segment === link.url ? "page" : undefined}
                    href={link.url == undefined ? "." : link.url}
                    >{link.label}</a
                >
            {/if}
        </li>
    {/each}
</ul>

<style>
    [aria-current] {
        position: relative;
        display: inline-block;
    }

    [aria-current]::after {
        position: absolute;
        content: "";
        width: calc(100% - 1em);
        height: 2px;
        background-color: rgb(255, 62, 0);
        display: block;
        bottom: -1px;
    }

    a {
        text-decoration: none;
        padding: 1em 0.5em;
        display: block;
    }
    ul {
        margin: 0;
        padding: 0;
    }

    /* clearfix */
    ul::after {
        content: "";
        display: block;
        clear: both;
    }

    li {
        display: block;
        float: left;
    }
</style>
