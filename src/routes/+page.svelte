<script>
    import Menu from "../components/Menu.svelte";
</script>

<!-- ─── HERO ─── -->
<section class="hero">
    <div class="hero-text">
        <span class="eyebrow">Benvenuti</span>
        <h1>Schmecke die beste<br>Pizza & Pasta<br>der Stadt</h1>
        <p>Authentische Rezepte, frische Zutaten,<br>unvergleichlicher Geschmack.</p>
        <a href="#menu" class="cta">Speisekarte ansehen</a>
    </div>

</section>

<!-- ─── ÖFFNUNGSZEITEN ─── -->
<section class="hours" id="oeffnungszeiten">
    <div class="hours-inner">
        <div class="hours-left">
            <span class="eyebrow-dark">Wir freuen uns auf Sie</span>
            <h2>Öffnungszeiten</h2>
            <p>Für Reservierungen rufen Sie uns gerne an – wir freuen uns auf Ihren Besuch.</p>
            <a href="tel:+4991948208" class="phone-cta">
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.72 12a19.79 19.79 0 0 1-3.07-8.63A2 2 0 0 1 3.72 1.18h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6.29 6.29l1.1-1.06a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7a2 2 0 0 1 1.72 2.02z"/></svg>
                +49 9194 8208
            </a>
        </div>

        <div class="hours-card">
            <div class="hours-row closed">
                <span>Montag</span>
                <span>Geschlossen</span>
            </div>
            <div class="hours-row">
                <span>Dienstag</span>
                <span>17:00 – 22:00 Uhr</span>
            </div>
            <div class="hours-row">
                <span>Mittwoch</span>
                <span>17:00 – 22:00 Uhr</span>
            </div>
            <div class="hours-row">
                <span>Donnerstag</span>
                <span>17:00 – 22:00 Uhr</span>
            </div>
            <div class="hours-row">
                <span>Freitag</span>
                <span>17:00 – 22:00 Uhr</span>
            </div>
            <div class="hours-row">
                <span>Samstag</span>
                <span>17:00 – 22:00 Uhr</span>
            </div>
            <div class="hours-row">
                <span>Sonntag</span>
                <span>17:00 – 22:00 Uhr</span>
            </div>
        </div>
    </div>
</section>

<!-- ─── MENU ─── -->
<section class="menu-section" id="menu">
    <div class="menu-header">
        <span class="eyebrow-dark">Was darf es sein?</span>
        <div class="menu-title-row">
            <h2>Unsere Speisekarte</h2>
            <a href="/dokuments/menu-tsv.pdf" target="_blank" rel="noopener" class="pdf-btn">
                <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
                Speisekarte als PDF
            </a>
        </div>
    </div>
    <Menu/>
</section>

<style>
    /* ─── HERO ─── */
    .hero {
        min-height: 100vh;
        display: flex;
        align-items: center;
        background-image:
            linear-gradient(105deg, rgba(10,10,10,0.97) 40%, rgba(10,10,10,0.55) 70%, rgba(10,10,10,0.1) 100%),
            url('/images/background-image.jpg');
        background-size: cover;
        background-position: center;
    }

    .hero-text {
        max-width: 1100px;
        width: 90%;
        margin: auto;
        padding-top: 6rem;
        padding-bottom: 4rem;
    }

    .eyebrow {
        display: block;
        color: var(--red);
        font-size: 0.75rem;
        font-weight: 700;
        letter-spacing: 4px;
        text-transform: uppercase;
        margin-bottom: 1.2rem;
    }

    .hero-text h1 {
        color: white;
        margin-bottom: 1.4rem;
    }

    .hero-text p {
        color: rgba(255, 255, 255, 0.68);
        font-size: 1rem;
        line-height: 1.75;
        margin-bottom: 2.5rem;
    }

    .cta {
        display: inline-block;
        padding: 15px 38px;
        background: var(--red);
        color: white !important;
        font-weight: 600;
        font-size: 0.92rem;
        letter-spacing: 0.5px;
        border-radius: 4px;
        transition: background 200ms ease, transform 200ms ease, box-shadow 200ms ease;
        box-shadow: 0 8px 24px rgba(175, 30, 34, 0.35);
    }

    .cta:hover {
        background: #961a1e;
        transform: translateY(-2px);
        box-shadow: 0 12px 32px rgba(175, 30, 34, 0.45);
    }


    /* ─── HOURS ─── */
    .hours {
        background: var(--warm);
        padding: 7rem 5%;
    }

    .hours-inner {
        max-width: 1100px;
        margin: auto;
        display: grid;
        grid-template-columns: 1fr 1.1fr;
        gap: 5rem;
        align-items: center;
    }

    .eyebrow-dark {
        display: block;
        color: var(--red);
        font-size: 0.75rem;
        font-weight: 700;
        letter-spacing: 4px;
        text-transform: uppercase;
        margin-bottom: 0.9rem;
    }

    .hours-left h2 {
        margin-bottom: 1rem;
    }

    .hours-left p {
        color: var(--gray);
        font-size: 0.95rem;
        line-height: 1.75;
        margin-bottom: 1.75rem;
        max-width: 360px;
    }

    .phone-cta {
        display: inline-flex;
        align-items: center;
        gap: 9px;
        color: var(--red) !important;
        font-weight: 700;
        font-size: 1.1rem;
        transition: opacity 200ms;
    }

    .phone-cta svg {
        color: var(--red);
    }

    .phone-cta:hover {
        opacity: 0.75;
    }

    .hours-card {
        background: white;
        border-radius: 14px;
        overflow: hidden;
        box-shadow: 0 6px 32px rgba(0, 0, 0, 0.07);
    }

    .hours-row {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1.1rem 1.75rem;
        border-bottom: 1px solid var(--border);
        font-size: 0.92rem;
    }

    .hours-row:last-child {
        border-bottom: none;
    }

    .hours-row span:first-child {
        font-weight: 500;
        color: var(--dark);
    }

    .hours-row span:last-child {
        color: var(--gray);
    }

    .hours-row.closed span:first-child {
        color: var(--gray);
    }

    .hours-row.closed span:last-child {
        color: var(--red);
        font-weight: 600;
        font-size: 0.85rem;
        letter-spacing: 0.5px;
    }

    /* ─── MENU SECTION ─── */
    .menu-section {
        padding: 7rem 5%;
        background: white;
    }

    .menu-header {
        max-width: 1100px;
        margin: 0 auto 3rem;
    }

    .menu-title-row {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 1rem;
    }

    .menu-title-row h2 {
        font-size: clamp(1.6rem, 2vw + 1rem, 2.2rem);
    }

    .pdf-btn {
        display: inline-flex;
        align-items: center;
        gap: 7px;
        color: var(--gray) !important;
        font-size: 0.85rem;
        font-weight: 500;
        border: 1px solid var(--border);
        padding: 9px 18px;
        border-radius: 7px;
        transition: all 200ms ease;
        white-space: nowrap;
    }

    .pdf-btn svg {
        color: var(--gray);
        transition: color 200ms;
    }

    .pdf-btn:hover {
        color: var(--dark) !important;
        border-color: var(--dark);
        background: var(--warm);
    }

    .pdf-btn:hover svg {
        color: var(--dark);
    }

    /* ─── RESPONSIVE ─── */
    @media (max-width: 900px) {
        .hero {
            background-image:
                linear-gradient(to bottom, rgba(10,10,10,0.92) 50%, rgba(10,10,10,0.75) 100%),
                url('/images/background-image.jpg');
            justify-content: center;
        }

        .hero-text {
            max-width: 100%;
        }

        .hours-inner {
            grid-template-columns: 1fr;
            gap: 2.5rem;
        }

        .hours-left p {
            max-width: 100%;
        }

        .menu-section {
            padding: 5rem 5%;
        }
    }

    @media (max-width: 500px) {
        .hero {
            align-items: flex-end;
            padding-bottom: 5rem;
        }

        .hours {
            padding: 5rem 5%;
        }
    }
</style>
