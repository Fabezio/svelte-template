<script>
    import appId from '../data/appId.js';
    export let tab= "nouvelle page"
    export let heading= "nouveau titre" 
    function firstLetterCapitalize(str) {
        return str.charAt(0).toUpperCase()+str.slice(1)
    }
</script>

<svelte:head>
    <title>
        {appId.appname} | {firstLetterCapitalize(tab)}
        
    </title>
</svelte:head>
<h1>{firstLetterCapitalize(heading)}</h1>