<svelte:head>
    <title>Impressum – Ristorante TSV</title>
</svelte:head>

<article class="legal-page">
    <div class="inner">
        <a href="/" class="back-link">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="15 18 9 12 15 6"/></svg>
            Zurück zur Startseite
        </a>

        <h1>Impressum</h1>

        <section>
            <h2>Angaben gemäß § 5 TMG</h2>
            <p>
                Ristorante TSV<br>
                Sportplatzstraße 4<br>
                91320 Ebermannstadt
            </p>
        </section>

        <section>
            <h2>Kontakt</h2>
            <p>
                Telefon: <a href="tel:+4991948208">+49 9194 8208</a><br>
                E-Mail: <span class="placeholder">[E-Mail-Adresse einfügen]</span>
            </p>
        </section>

        <section>
            <h2>Verantwortlich für den Inhalt nach § 55 Abs. 2 RStV</h2>
            <p>
                <span class="placeholder">[Name des Inhabers]</span><br>
                Sportplatzstraße 4<br>
                91320 Ebermannstadt
            </p>
        </section>

        <section>
            <h2>Haftungsausschluss</h2>
            <h3>Haftung für Inhalte</h3>
            <p>
                Als Diensteanbieter sind wir gemäß § 7 Abs. 1 TMG für eigene Inhalte auf diesen Seiten nach den allgemeinen Gesetzen verantwortlich. Nach §§ 8 bis 10 TMG sind wir als Diensteanbieter jedoch nicht verpflichtet, übermittelte oder gespeicherte fremde Informationen zu überwachen oder nach Umständen zu forschen, die auf eine rechtswidrige Tätigkeit hinweisen.
            </p>
            <p>
                Verpflichtungen zur Entfernung oder Sperrung der Nutzung von Informationen nach den allgemeinen Gesetzen bleiben hiervon unberührt. Eine diesbezügliche Haftung ist jedoch erst ab dem Zeitpunkt der Kenntnis einer konkreten Rechtsverletzung möglich. Bei Bekanntwerden von entsprechenden Rechtsverletzungen werden wir diese Inhalte umgehend entfernen.
            </p>
            <h3>Haftung für Links</h3>
            <p>
                Unser Angebot enthält Links zu externen Websites Dritter, auf deren Inhalte wir keinen Einfluss haben. Deshalb können wir für diese fremden Inhalte auch keine Gewähr übernehmen. Für die Inhalte der verlinkten Seiten ist stets der jeweilige Anbieter oder Betreiber der Seiten verantwortlich.
            </p>
            <h3>Urheberrecht</h3>
            <p>
                Die durch die Seitenbetreiber erstellten Inhalte und Werke auf diesen Seiten unterliegen dem deutschen Urheberrecht. Die Vervielfältigung, Bearbeitung, Verbreitung und jede Art der Verwertung außerhalb der Grenzen des Urheberrechtes bedürfen der schriftlichen Zustimmung des jeweiligen Autors bzw. Erstellers.
            </p>
        </section>
    </div>
</article>

<style>
    .legal-page {
        padding: 10rem 5% 6rem;
        min-height: 100vh;
        background: var(--warm);
    }

    .inner {
        max-width: 720px;
        margin: auto;
    }

    .back-link {
        display: inline-flex;
        align-items: center;
        gap: 6px;
        font-size: 0.85rem;
        color: var(--gray) !important;
        margin-bottom: 2.5rem;
        transition: color 150ms;
    }

    .back-link:hover {
        color: var(--dark) !important;
    }

    .back-link svg {
        color: inherit;
    }

    h1 {
        font-size: clamp(1.8rem, 3vw, 2.6rem);
        font-weight: 700;
        margin-bottom: 2.5rem;
        padding-bottom: 1.25rem;
        border-bottom: 2px solid var(--border);
    }

    section {
        margin-bottom: 2.5rem;
    }

    h2 {
        font-size: 1.05rem;
        font-weight: 700;
        color: var(--dark);
        margin-bottom: 0.75rem;
        text-transform: uppercase;
        letter-spacing: 0.5px;
        font-size: 0.82rem;
        color: var(--red);
    }

    h3 {
        font-size: 0.95rem;
        font-weight: 600;
        margin: 1.25rem 0 0.5rem;
    }

    p {
        font-size: 0.92rem;
        color: var(--gray);
        line-height: 1.8;
        margin-bottom: 0.75rem;
    }

    a {
        color: var(--red) !important;
    }

    a:hover {
        text-decoration: underline;
    }

    .placeholder {
        background: #fef3cd;
        padding: 1px 6px;
        border-radius: 3px;
        font-style: italic;
        color: #856404;
    }
</style>
