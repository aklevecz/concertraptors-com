<script>
    let {children} = $props()
</script>

{@render children()}

<style>
    :global(html) {
        --primary-color: #f9f9f9b4;
        --secondary-color: #33aaff;
    }
    :global(body) {
        margin: 0;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
        background-color: var(--primary-color);
        color: var(--secondary-color)
    }
    :global(a) {
        color: var(--secondary-color);
    }
</style>