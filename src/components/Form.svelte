<script>
    import { prevent_default } from "svelte/internal";

    let entry = "";
    let validateEntry = "";
    function handleSubmit(event) {
        validateEntry = entry;
        console.log(entry);
        return validateEntry;
    }
</script>

<form on:submit|preventDefault={handleSubmit}>
    <input type="text" bind:value={entry} placeholder="entry" />
    <button type="submit">Imprimer</button>
</form>
<p>{validateEntry}</p>
