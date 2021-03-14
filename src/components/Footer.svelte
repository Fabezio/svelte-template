<script>
    import appId from '../data/appId.js'
    const {appname, applink} = appId
    </script>

<footer>
    <span>
        {appname} @ {new Date().getFullYear()}
    </span>
    <span>
        mon code source : <a href={applink+appname} target="_blank">{appname}</a>

    </span>
    <span>
        Fait avec :
        <img src="svelte_js.png" alt="logo svelte" width="100">
    </span>

</footer>

<style>
    footer {
        position: absolute;
        bottom: 0;
        display: block;
        width: 100%;
        text-align: center;
        opacity: 75%;
        height: 3rem;
    }
    span {margin: 0 1rem;}
    a {
        text-decoration: none;
    }
    img {
        position: relative;
        top: 9px;
        display: inline-block;
    }
</style>