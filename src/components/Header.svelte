<script>
    import Nav from './navbar/Nav.svelte'
    
    let title;
    export let segment;
</script>
<header>
    <Nav {segment} />
    
</header>