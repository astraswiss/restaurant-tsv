<script>
    const year = new Date().getFullYear();
</script>

<footer>
    <div class="footer-inner">
        <div class="col brand">
            <h4>Ristorante TSV</h4>
            <p>Sportplatzstraße 4<br>91320 Ebermannstadt</p>
            <a href="tel:+4991948208" class="phone">+49 9194 8208</a>
        </div>

        <div class="col">
            <h4>Öffnungszeiten</h4>
            <ul>
                <li><span>Dienstag – Sonntag</span><span>17:00 – 22:00 Uhr</span></li>
                <li class="closed"><span>Montag</span><span>Geschlossen</span></li>
            </ul>
        </div>

        <div class="col links">
            <h4>Rechtliches</h4>
            <a href="/impressum">Impressum</a>
            <a href="/datenschutz">Datenschutz</a>
        </div>
    </div>

    <div class="footer-bottom">
        <p>© {year} Ristorante TSV · Alle Rechte vorbehalten</p>
    </div>
</footer>

<style>
    footer {
        background: #1c1c1e;
        color: rgba(255, 255, 255, 0.7);
    }

    .footer-inner {
        max-width: 1100px;
        margin: auto;
        padding: 4rem 5% 3rem;
        display: grid;
        grid-template-columns: 1.4fr 1fr 0.8fr;
        gap: 3rem;
    }

    .col h4 {
        color: white;
        font-size: 0.8rem;
        font-weight: 600;
        letter-spacing: 2.5px;
        text-transform: uppercase;
        margin-bottom: 1.2rem;
    }

    /* Brand col */
    .brand h4 {
        margin-bottom: 1rem;
    }

    .brand p {
        font-size: 0.9rem;
        line-height: 1.8;
        margin-bottom: 0.75rem;
    }

    .brand .phone {
        color: rgba(255, 255, 255, 0.9);
        font-weight: 500;
        font-size: 0.95rem;
        transition: color 200ms;
    }

    .brand .phone:hover {
        color: #af1e22;
    }

    /* Hours col */
    ul {
        display: flex;
        flex-direction: column;
        gap: 0.6rem;
    }

    ul li {
        display: flex;
        justify-content: space-between;
        gap: 1rem;
        font-size: 0.88rem;
    }

    ul li span:first-child {
        color: rgba(255, 255, 255, 0.6);
    }

    ul li span:last-child {
        color: rgba(255, 255, 255, 0.85);
        text-align: right;
    }

    ul li.closed span:last-child {
        color: #af1e22;
    }

    /* Links col */
    .links {
        display: flex;
        flex-direction: column;
    }

    .links a {
        color: rgba(255, 255, 255, 0.6);
        font-size: 0.9rem;
        margin-bottom: 0.6rem;
        transition: color 200ms;
    }

    .links a:hover {
        color: white;
    }

    /* Bottom bar */
    .footer-bottom {
        border-top: 1px solid rgba(255, 255, 255, 0.08);
        text-align: center;
        padding: 1.25rem 5%;
    }

    .footer-bottom p {
        font-size: 0.82rem;
        color: rgba(255, 255, 255, 0.35);
    }

    @media (max-width: 768px) {
        .footer-inner {
            grid-template-columns: 1fr;
            gap: 2rem;
            padding-bottom: 2rem;
        }
    }
</style>
