<script>
    import Fade from "$lib/Fade.svelte";
</script>

<Fade>
    <div class="out">
        <div class="in">
            <div class="box">
                <h2>GET ONLINE</h2>
                <p>
                    Let’s help you take your business online. We design full
                    stack web servers in the cloud that keep your business and
                    service always available to you and your clients from
                    anywhere in the world.
                </p>
                <div class="button-center">
                    <a class="button" href="/#">Learn More</a>
                </div>
            </div>
            <div class="box" />
            <div class="box" />
        </div>
    </div>
</Fade>

<style>
    h2 {
        font-family: "Roboto", sans-serif;
    }
    .out {
        position: relative;
        width: 100%;
        min-height: calc(100vh - var(--nav-height));
    }
    .in {
        position: absolute;
        width: 300px;
        height: 400px;
        left: 50%;
        transform: translate(-50%, 40px);
    }
    .in h2 {
        text-align: center;
        padding: 1em 2em;
    }
    .in p {
        text-align: center;
        padding: 0 2em;
    }
    .box {
        position: absolute;
        width: 100%;
        height: 100%;
        transform-origin: -20% 90%;
        border-radius: 10px;
    }

    .in .box:nth-child(1) {
        border: 2px solid hsl(175, 98%, 36%);
        z-index: 4;
    }

    .in .box:nth-child(2) {
        /* background-color: red; */
        z-index: -2;
        animation-name: tilt-child-2;
        animation-fill-mode: forwards;
        animation-duration: 1s;
        border: 3px solid rgb(154, 149, 167);
    }

    .in .box:nth-child(3) {
        border: 2px solid lightblue;
        z-index: -3;
        animation: tilt-child-3 1s forwards;
    }

    .button {
        display: inline-block;
        padding: 0.5em;
        margin: 0 auto;
        border-radius: 5px;
        text-decoration: none;
        border: 2px solid var(--color-teal);
    }

    .button-center {
        text-align: center;
    }

    @keyframes shadow {
        from {
            box-shadow: 2px 2px var(--color-teal-alpha);
        }
        to {
            box-shadow: 10px 15px var(--color-teal-alpha);
        }
    }

    @keyframes tilt-child-2 {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(20deg);
        }
    }

    @keyframes tilt-child-3 {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(-20deg);
        }
    }
</style>
