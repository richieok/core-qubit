<div>
    <slot></slot>
</div>

<style>
    div {
        animation-name: fade;
        animation-duration: 1s;
    }
    @keyframes fade {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
</style>