<script>
    import appId from '../data/appId.js';
    export let title = "nouvelle page";
</script>

<svelte:head>
    <title>
        {appId.appname} | {title}
        
    </title>
</svelte:head>
<h1>{title}</h1>