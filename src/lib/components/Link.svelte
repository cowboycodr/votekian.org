<script>
    export let href = "/";
</script>

<div>
    <a {href}>
        <slot />
    </a>
</div>

<style>
    a {
        font-size: .9rem;
        color: rgba(0, 149, 255, 0.6);
    }
</style>