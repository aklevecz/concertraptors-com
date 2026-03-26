<script>
    import { marked } from 'marked';
    import ramblingsRaw from './manifesto.md?raw';

    const html = marked(ramblingsRaw);
</script>

<svelte:head>
    <title>CONCERT RAPTORS</title>
    <meta name="description" content="Concert Raptors est. 2015 - Music belongs to us." />
    <meta property="og:title" content="CONCERT RAPTORS" />
    <meta property="og:description" content="Music belongs to us, and it is time to burn down the structures that tell us otherwise." />
    <meta property="og:image" content="https://concertraptors.com/ogimage.png" />
    <meta property="og:url" content="https://concertraptors.com" />
    <meta name="twitter:card" content="summary_large_image" />
</svelte:head>

<article>
    <header>
        <img src="/raptor-svg.svg" alt="Concert Raptors" class="logo" />
    </header>

    <div class="content">
        {@html html}
    </div>
</article>

<style>
    article {
        min-height: 100vh;
        max-width: 680px;
        margin: 0 auto;
        padding: 4rem 2rem 6rem;
        color: #e8e8e8;
        background: #0a0a0a;
        text-transform: lowercase;
    }

    :global(body) {
        background: #0a0a0a !important;
    }

    header {
        margin-bottom: 4rem;
        text-align: center;
    }

    .logo {
        width: 80px;
        display: block;
        margin: 0 auto 2rem;
    }

    .content :global(h2) {
        font-size: 0.75rem;
        font-weight: 700;
        letter-spacing: 0.25em;
        text-transform: lowercase;
        color: #ff3333;
        margin-bottom: 1.5rem;
        margin-top: 3rem;
    }

    .content :global(p) {
        font-size: 1.1rem;
        line-height: 1.8;
        color: #e8e8e8;
        margin: 0 0 1.5rem;
        font-weight: 300;
    }

    .content :global(p:first-child) {
        font-size: 1.4rem;
        line-height: 1.7;
        color: #fff;
        font-weight: 400;
    }

    .content :global(hr) {
        border: none;
        margin: 4rem 0 2rem;
    }

    .content :global(hr + p) {
        font-size: 1.6rem;
        font-weight: 700;
        color: #fff;
        letter-spacing: 0.02em;
        text-align: center;
    }

    @media (max-width: 640px) {
        article {
            padding: 2.5rem 1.25rem 4rem;
        }

        .content :global(p:first-child) {
            font-size: 1.15rem;
        }

        .content :global(p) {
            font-size: 1rem;
        }

        .content :global(hr + p) {
            font-size: 1.3rem;
        }
    }
</style>
