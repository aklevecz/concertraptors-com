<script>
    /** @type {{ data: import('./$types').PageData }} */
    let { data } = $props();

    const links = [
        {
            title: "Event page and tickets",
            url: "https://tickets.raptor.pizza",
            icon: "🎟️"
        },
        {
            title: "Download Raptor iOS App to view tickets and interact at the show",
            url: "https://app.raptor.pizza/testflight",
            icon: "🍏"
        },
        {
            title: "View your tickets on web browser",
            url: "https://tickets.raptor.pizza/profile",
            icon: "👤"
        }
    ];

    const profile = {
        name: "CONCERT RAPTOR TAKEOVER 🌸 FAIGHT COLLECTIVE",
        // bio: "Full-stack developer | Open source enthusiast | Tech writer",
        avatar: "/raptor-svg.svg"
    };
</script>

<div class="container">
    <div class="profile">
        <img
            src={profile.avatar}
            alt={profile.name}
            class="avatar"
        />
        <h1>{profile.name}</h1>
        <p class="bio">{profile.bio}</p>
    </div>

    <div class="links">
        {#each links as link}
            <a
                href={link.url}
                target="_blank"
                rel="noopener noreferrer"
                class="link-card"
            >
                <span class="icon">{link.icon}</span>
                <span class="title">{link.title}</span>
            </a>
        {/each}
    </div>

    <footer>
        <p>© 2024 {profile.name}. Made with ❤️</p>
    </footer>
</div>

<style>
    .container {
        min-height: 100vh;
        padding: 3rem 1rem;
        background: linear-gradient(135deg, #00000000 0%, #ff0000 100%);
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    }

    .profile {
        max-width: 28rem;
        margin: 0 auto;
        text-align: center;
        margin-bottom: 2rem;
    }

    .avatar {
        width: 6rem;
        height: 6rem;
        border-radius: 50%;
        margin: 0 auto 1rem;
        border: 4px solid white;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    h1 {
        color: white;
        font-size: 1.5rem;
        margin-bottom: 0.5rem;
    }

    .bio {
        color: rgba(255, 255, 255, 0.9);
        margin: 0;
    }

    .links {
        max-width: 28rem;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .link-card {
        display: flex;
        align-items: center;
        padding: 1rem;
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(8px);
        border: 1px solid rgba(255, 255, 255, 0.2);
        border-radius: 0.5rem;
        color: white;
        text-decoration: none;
        transition: all 0.3s ease;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .link-card:hover {
        background: rgba(255, 255, 255, 0.2);
        transform: translateY(-2px);
        box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
    }

    .icon {
        font-size: 1.5rem;
        margin-right: 1rem;
    }

    .title {
        font-weight: 500;
    }

    footer {
        max-width: 28rem;
        margin: 3rem auto 0;
        text-align: center;
        color: rgba(255, 255, 255, 0.7);
        font-size: 0.875rem;
    }

    @media (max-width: 640px) {
        .container {
            padding: 2rem 1rem;
        }

        .avatar {
            width: 5rem;
            height: 5rem;
        }

        h1 {
            font-size: 1.25rem;
        }
    }
</style>