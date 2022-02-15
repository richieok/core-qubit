<script>
    import '../app.css';
    import Nav from "$lib/Nav.svelte";
</script>
<img class="bg" src="/gradient-bg.jpg" alt="background">

<Nav/>
<main>
    <slot/>
</main>

<style>
    img.bg {
        min-height: 100%;
        min-width: 1920px;

        width: 100%;
        height: auto;

        position: fixed;
        top: 0;
        left: 0;
        z-index: -5;
        opacity: .9;
    }

    @media screen and (max-width: 1920px) {
        img.bg {
            left: 50%;
            margin-left: -960px;
        }
    }
</style>
