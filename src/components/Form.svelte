<script>
    import { prevent_default } from "svelte/internal";
    import Input from "./Input.svelte";

    let entry = "";
    let validateEntry = "";
    let username="";
    let surname="";
    const newData = [
        username,
        surname,
        entry

    ]
    console.log(newData)
    
    
    function handleSubmit(e) {
        
        if (newData.length == 3) {
            console.log(newData);
            return newData;
        } 
    }
    
    $: console.log(`identifiant: ${username}`)
        console.log(`nom: ${surname}`)
        console.log(`entrée: ${entry}`)

</script>

<form on:submit|preventDefault={handleSubmit}>
    <Input val="{username}" label="Entrez votre identifiant: " />
    <Input val="{surname}" label="Entrez votre nom de famille: " />
    <input type="text" bind:value={entry}  placeholder="entry" />
    <button type="submit">Imprimer</button>
</form>
{#each newData as data}
<p>{data}</p>
{/each}
