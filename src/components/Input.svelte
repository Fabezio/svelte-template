<script>
    export let val = "";
    export let label = "entrez votre texte ici";
    
</script>

<style>
    input {
        display: block;
    }
</style>

<input type="text" value={val} on:input={e=>e.target.val} placeholder={label}>