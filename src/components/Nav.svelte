<header>
    <nav>
        <a href="/">
            <img src="/images/tsv-logo.svg" alt="Ristorante TSV">
        </a>
        <div class="contact">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#FFD700" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.72 12a19.79 19.79 0 0 1-3.07-8.63A2 2 0 0 1 3.72 1.18h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6.29 6.29l1.1-1.06a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7a2 2 0 0 1 1.72 2.02z"/></svg>
            <a href="tel:+4991948208">+49 9194 8208</a>
        </div>
    </nav>
</header>

<style>
    header {
        width: 100%;
        position: absolute;
        top: 0;
        left: 0;
        z-index: 100;
    }

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1.5rem 5%;
        max-width: 1300px;
        margin: auto;
    }

    .contact {
        display: flex;
        align-items: center;
        gap: 8px;
        transition: opacity 200ms ease;
    }

    .contact:hover {
        opacity: 0.75;
    }

    .contact svg {
        color: #FFD700;
        flex-shrink: 0;
    }

    img {
        width: 88px;
    }

    a {
        color: white;
        font-size: 0.95rem;
        font-weight: 500;
    }
</style>
