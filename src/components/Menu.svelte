<script>
    let active = 'pizzen';

    const tabs = [
        { id: 'pizzen',    label: 'Pizzen' },
        { id: 'pasta',     label: 'Pasta' },
        { id: 'salate',    label: 'Salate & Vorspeisen' },
        { id: 'schnitzel', label: 'Schnitzel' },
        { id: 'dessert',   label: 'Dessert' },
    ];

    const pizzen = [
        { nr: '41', name: 'Margherita',       desc: 'Tomatensoße und Käse',                                      price: '8,50 €' },
        { nr: '42', name: 'Salame',           desc: 'Salami',                                                    price: '9,50 €' },
        { nr: '43', name: 'Prosciutto',       desc: 'Schinken',                                                  price: '9,50 €' },
        { nr: '44', name: 'Christina',        desc: 'Salami, Pilze',                                             price: '10,00 €' },
        { nr: '45', name: 'Romana',           desc: 'Schinken, Pilze',                                           price: '10,00 €' },
        { nr: '46', name: 'Hawaii',           desc: 'Schinken und Ananas',                                       price: '10,50 €' },
        { nr: '47', name: 'Contessa',         desc: 'Salami, Schinken, Pilze',                                   price: '11,20 €' },
        { nr: '48', name: 'Tonno',            desc: 'Thunfisch und Zwiebeln',                                    price: '11,90 €' },
        { nr: '49', name: 'Parma Speziale',   desc: 'Parmaschinken, Rucola, Parmesan',                           price: '13,50 €' },
        { nr: '50', name: 'Frutti di Mare',   desc: 'Meeresfrüchte, Knoblauch',                                  price: '13,50 €' },
        { nr: '51', name: 'Sophia Loren',     desc: 'Schinken, Salami, Paprika, Ei',                             price: '12,90 €' },
        { nr: '52', name: 'Quattro Stagioni', desc: 'Schinken, Artischocken, Pilze, Spargel',                    price: '12,90 €' },
        { nr: '53', name: 'Ricotta Spinaci',  desc: 'Schafskäse, Spinat',                                        price: '11,50 €' },
        { nr: '54', name: 'Quattro Formaggi', desc: '4 Käsesorten',                                              price: '12,90 €' },
        { nr: '55', name: 'Vegetale',         desc: 'Frisches Gemüse',                                           price: '12,90 €' },
        { nr: '56', name: 'Mozzarella',       desc: 'Mozzarella, Tomaten, Basilikum',                            price: '11,50 €' },
        { nr: '57', name: 'Colosseo',         desc: 'Schinken, Zwiebeln, Pilze, Peperoni',                       price: '12,90 €' },
        { nr: '58', name: 'Calzone',          desc: 'Teigtasche mit Schinken, Pilze',                            price: '12,50 €' },
        { nr: '59', name: 'Pizza Stella',     desc: 'Pilze, Schinken, Spargel, Oliven, Kapern, Sardellen',       price: '13,80 €' },
        { nr: '60', name: 'Spinaci Salmone',  desc: 'Lachs, Spinat, Knoblauch',                                  price: '13,90 €' },
    ];

    const pasta = [
        { nr: '80', name: 'Spaghetti Napoli',                   desc: 'Mit Tomatensoße',                                                   price: '9,90 €' },
        { nr: '81', name: 'Spaghetti Bolognese',                desc: 'Mit Hackfleisch-Tomatensoße',                                       price: '11,50 €' },
        { nr: '82', name: 'Spaghetti Aglio e Olio e Peperoncino', desc: 'Knoblauch, Olivenöl und Parmesanstreifen',                        price: '10,50 €' },
        { nr: '83', name: 'Spaghetti Carbonara',                desc: 'Mit Schinken-Sahnesoße, Ei',                                        price: '11,50 €' },
        { nr: '84', name: 'Spaghetti Scampi',                   desc: 'Mit frischen Tomaten, Scampi und Knoblauch',                        price: '14,50 €' },
        { nr: '85', name: 'Spaghetti Frutti di Mare',           desc: 'Meeresfrüchte und Knoblauch in einer Weißweinsoße',                 price: '14,50 €' },
        { nr: '86', name: 'Tortellini al Chef',                 desc: 'Pilze, Schinken und Erbsen in Rosésoße',                            price: '12,90 €' },
        { nr: '87', name: 'Tortellini Panna e Prosciutto',      desc: 'Schinken und Sahne',                                                price: '11,50 €' },
        { nr: '88', name: 'Tagliatelle Salmone',                desc: 'Mit Lachs und Brokkoli',                                            price: '14,50 €' },
        { nr: '89', name: 'Penne Porcini',                      desc: 'Steinpilze in Sahnesoße',                                           price: '13,50 €' },
        { nr: '90', name: 'Tagliatelle della Casa',             desc: 'Steinpilze, Scampi, Rucola, Cherrytomaten und Parmesan',            price: '15,80 €' },
        { nr: '91', name: 'Tagliatelle al Chef',                desc: 'Pilze, Schinken und Erbsen in Rosésoße',                            price: '12,90 €' },
        { nr: '92', name: 'Rigatoni Melanzane',                 desc: 'Auberginen und Zucchini in Rosésoße',                               price: '11,50 €' },
        { nr: '93', name: 'Penne Diavolo',                      desc: 'Mit scharfer Tomatensoße',                                          price: '10,50 €' },
        { nr: '94', name: 'Gnocchi Speciali',                   desc: 'Mit Paprika, Gorgonzola und Spinat in Rosésoße',                    price: '12,90 €' },
        { nr: '95', name: 'Lasagne al Forno',                   desc: 'Mit Hackfleisch',                                                   price: '12,90 €' },
        { nr: '96', name: 'Tortellini al Forno',                desc: 'Mit Erbsen, Schinken überbacken',                                   price: '12,90 €' },
        { nr: '97', name: 'Rigatoni al Forno',                  desc: 'Mit Erbsen, Schinken und Bolognese-Sahnesoße überbacken',           price: '12,90 €' },
        { nr: '98', name: 'Combinazione al Forno',              desc: 'Verschiedene Nudeln in Bolognesesoße überbacken',                   price: '12,90 €' },
    ];

    const salate = [
        { nr: '1',  name: 'Insalata Mista Piccola',        desc: 'Kleiner gemischter Salat',                                                           price: '6,50 €' },
        { nr: '2',  name: 'Verdura alla Griglia',          desc: 'Gemischtes Gemüse mit frisch gebackenem Brot',                                       price: '11,50 €' },
        { nr: '3',  name: 'Bruschetta',                    desc: 'Pizzabrot mit Tomaten, Rucola und Parmesan',                                          price: '7,20 €' },
        { nr: '4',  name: 'Bruschetta della Casa',         desc: 'Geröstetes Brot mit Tomaten, Rucola, Knoblauch, Parmesan und Basilikum',              price: '9,50 €' },
        { nr: '5',  name: 'Caprese',                       desc: 'Büffelmozzarella mit Tomaten und Basilikum',                                          price: '7,50 €' },
        { nr: '6',  name: 'Ricotta Calda',                 desc: 'Überbackener Schafskäse',                                                             price: '6,50 €' },
        { nr: '7',  name: 'Carpaccio Rucola e Parmigiano', desc: 'Mariniertes Rinderfilet mit Rucola, Zitrone und Parmesanstreifen',                    price: '9,50 €' },
        { nr: '8',  name: 'Crema Pomodoro',                desc: 'Hausgemachte Tomatencremesuppe',                                                      price: '6,50 €' },
        { nr: '21', name: 'Insalata Mista Grande',         desc: 'Großer gemischter Salat',                                                             price: '8,50 €' },
        { nr: '22', name: 'Insalata Nizza',                desc: 'Mit Tomaten, Gurken, Rucola, Zwiebeln und Thunfisch',                                  price: '10,50 €' },
        { nr: '23', name: 'Insalata Tonno',                desc: 'Großer gemischter Salat mit Thunfisch',                                               price: '10,50 €' },
        { nr: '24', name: 'Insalata Fitness',              desc: 'Mit Garnelen und frischem Brot',                                                      price: '14,20 €' },
        { nr: '25', name: 'Insalata Capricciosa',          desc: 'Mit Tomaten, Schafskäse, Ei, Schinken und Thunfisch',                                 price: '12,50 €' },
        { nr: '26', name: 'Insalata della Casa',           desc: 'Mit Tomaten, Gurken, Mais, Paprika, Schafskäse, Oliven, Spargel und Ei',              price: '12,50 €' },
        { nr: '27', name: 'Insalata Tacchina',             desc: 'Großer gemischter Salat mit Putenbruststreifen',                                      price: '13,80 €' },
        { nr: '28', name: 'Insalata Salmone',              desc: 'Großer gemischter Salat mit gebratenen Lachsstreifen und gegrilltem Gemüse',          price: '14,20 €' },
    ];

    const schnitzel = [
        { nr: '75', name: 'Jägerschnitzel',      desc: 'Mit Pommes',    price: '12,80 €' },
        { nr: '76', name: 'Schnitzel Mamma Mia', desc: 'Mit Rigatoni',  price: '13,90 €' },
    ];

    const dessert = [
        { nr: '–', name: 'Tiramisù',   desc: 'Hausgemacht, traditioneller Klassiker', price: '6,20 €' },
        { nr: '–', name: 'Panna Cotta', desc: 'Hausgemacht, Fruchtsoße',              price: '5,50 €' },
    ];

    const sectionData = { pizzen, pasta, salate, schnitzel, dessert };
</script>

<div class="menu-wrap">
    <!-- Tabs -->
    <div class="tabs" role="tablist">
        {#each tabs as tab}
            <button
                class:active={active === tab.id}
                on:click={() => active = tab.id}
                role="tab"
                aria-selected={active === tab.id}
            >
                {tab.label}
            </button>
        {/each}
    </div>

    <!-- Panel -->
    <div class="panel" role="tabpanel">
        {#if active === 'pizzen'}
            <p class="panel-note">Ø 33 cm · Alle Pizzen mit Tomatensoße und Käse als Basis</p>
        {/if}
        <div class="items-grid">
            {#each sectionData[active] as item}
                <div class="item">
                    <div class="item-top">
                        <span class="item-name">
                            {#if item.nr !== '–'}<span class="item-nr">{item.nr}.</span>{/if}
                            {item.name}
                        </span>
                        <span class="item-price">{item.price}</span>
                    </div>
                    <p class="item-desc">{item.desc}</p>
                </div>
            {/each}
        </div>
    </div>
</div>

<style>
    .menu-wrap {
        max-width: 1100px;
        margin: auto;
    }

    /* ─── TABS ─── */
    .tabs {
        display: flex;
        gap: 0.5rem;
        flex-wrap: wrap;
        margin-bottom: 2.5rem;
        border-bottom: 2px solid var(--border);
        padding-bottom: 0;
    }

    .tabs button {
        background: none;
        border: none;
        cursor: pointer;
        font-family: inherit;
        font-size: 0.88rem;
        font-weight: 500;
        color: var(--gray);
        padding: 0.75rem 1.25rem;
        border-bottom: 2px solid transparent;
        margin-bottom: -2px;
        transition: color 150ms ease, border-color 150ms ease;
        white-space: nowrap;
    }

    .tabs button:hover {
        color: var(--dark);
    }

    .tabs button.active {
        color: var(--red);
        border-bottom-color: var(--red);
        font-weight: 600;
    }

    /* ─── PANEL ─── */
    .panel-note {
        font-size: 0.82rem;
        color: var(--gray);
        margin-bottom: 1.5rem;
        font-style: italic;
    }

    .items-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 0;
    }

    /* ─── ITEM ─── */
    .item {
        padding: 1rem 1.25rem;
        border-bottom: 1px solid var(--border);
        transition: background 150ms ease;
    }

    .item:hover {
        background: var(--warm);
    }

    /* Remove right border for even columns, add separator for odd */
    .item:nth-child(odd) {
        border-right: 1px solid var(--border);
    }

    .item-top {
        display: flex;
        justify-content: space-between;
        align-items: baseline;
        gap: 1rem;
        margin-bottom: 0.25rem;
    }

    .item-name {
        font-size: 0.92rem;
        font-weight: 600;
        color: var(--dark);
        line-height: 1.4;
    }

    .item-nr {
        color: var(--gray);
        font-weight: 400;
        font-size: 0.82rem;
        margin-right: 3px;
    }

    .item-price {
        font-size: 0.92rem;
        font-weight: 700;
        color: var(--red);
        white-space: nowrap;
        flex-shrink: 0;
    }

    .item-desc {
        font-size: 0.8rem;
        color: var(--gray);
        line-height: 1.5;
    }

    @media (max-width: 640px) {
        .items-grid {
            grid-template-columns: 1fr;
        }

        .item:nth-child(odd) {
            border-right: none;
        }

        .tabs button {
            font-size: 0.82rem;
            padding: 0.6rem 0.9rem;
        }
    }
</style>
