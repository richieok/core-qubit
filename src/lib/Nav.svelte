<script>
    import {page} from '$app/stores';
</script>

<nav>
    <div>

    </div>
    <ul>
        <li class:active={$page.url.pathname === '/'}><a href="/">Home</a></li>
        <!-- <li class:active={$page.url.pathname === '/blog'}><a href="/blog">Blog</a></li>
        <li class:active={$page.url.pathname === '/contact'}><a href="/contact">Contact</a></li>
        <li class:active={$page.url.pathname === '/about'}><a href="/about">About</a></li> -->
    </ul>
</nav>

<style>
    nav {
        display: flex;
        /* min-height: 3em; */
        height: var(--nav-height);
        margin-left: 1em;
        margin-right: 1em;;
    }
    ul {
        /* display: flex; */
        display: inline-flex;
        right: 0px;
        list-style: none;
    }

    ul > li {
        margin: 0.5em .2em;
        z-index: 5
    }

    .active a:link, a:visited {
        background-color: rgb(66, 77, 83);
        color: black;
        text-decoration: none;
        padding: .5em .5em;
        margin: .5em 0em;
        border: var(--nav-border) solid var(--color-teal);
        border-radius: 10px;
        display: inline-block;
    }

    a:link, a:visited {
        color: white;
        text-decoration: none;
        padding: .5em .5em;
        margin: .5em 0em;
        border: var(--nav-border) solid var(--color-teal);
        border-radius: 10px;
        display: inline-block;
    }

</style>