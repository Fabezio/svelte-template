<script>
    export let urlName = "";
    export let text = "bouton";
</script>

{#if urlName.length > 0}
    <a href="urlName">{text}</a>
{:else}
    <button>{text}</button>
{/if}

<style>
    button,
    a {
        box-sizing: border-box;
        border: 0px;
        border-radius: 7px;
        color: whitesmoke;
        text-transform: uppercase;
        padding: 10px 1rem;
        /* line-height: 1.1rem; */
        /* height: 2rem; */
        font-size: 1rem;
        /* transition-name:  */
        margin: 7px;
    }
    button {
        background: #0a0;
    }
    button:hover {
        background: #0a7;
        text-decoration: none;
    }
    a {
        background: teal;
        text-decoration: none;
    }
    a:hover {
        background: #07a;
    }
</style>
