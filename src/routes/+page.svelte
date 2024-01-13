<script>
    const baker = {
        navn: '[navn kommer]',
        telefon: '[telefonnummer kommer]',
        kjoretidspunkt: '[klokkeslett kommer]'
    }
    const brud = {
        navn: 'Frid',
        epost: 'fridbjugn@gmail.com',
        telefon: '94 89 94 36',
    }
    const brudgom = {
        navn: 'Larus',
        epost: 'larus93@gmail.com',
        telefon: '418 51 755',
    }
    const kjokemester = {
        navn: 'Toastmaster Isak (Frids bror)',
        epost: 'isakbjugn@gmail.com',
        telefon: '928 35 995',
    }
    const contactInformation = [brud, brudgom, kjokemester]
</script>

<main>
    <h1>Frid og Larus' bryllup</h1>
    <p style="text-align: center">Vi gifter oss 15. juni 2024!</p>
    <picture>
        <source srcset="frid-og-larus.webp" type="image/webp">
        <source srcset="frid-og-larus.jpg" type="image/jpg">
        <img src="frid-og-larus.jpg" alt="Smilende Frid og noe ukomfortabel Larus" />
    </picture>
    <p>
        Vi er utrolig takknemlig og kry over at så mange ønsker å komme til Vesterålen for å feire kjærligheten vår. Valget vårt for sted til bryllup falt på Kvitnes gård etter å ha opplevd atmosfæren på gården ved et besøk dit vinteren 2022, samt etter flere middager på Lille Kvitnes på Sortland. Vårt ønske er å få dele et særdeles godt måltid og tilbringe tid sammen med de vi er glade i.
    </p>
    <details>
        <summary><span class="summary-title">Registrering</span></summary>
        <iframe
          title="Gjesteregistrering (skjema)"
          src="https://docs.google.com/forms/d/e/1FAIpQLSf4K5RrZjA3-oifJuFVl5HVP-TykvU1thDPJR03Y5pGY8YxjA/viewform?embedded=true"
          width="488"
          height="704"
          frameborder="0"
          marginheight="0"
          marginwidth="0"
        />
    </details>
    <details>
        <summary><span class="summary-title">Kontaktinformasjon</span></summary>
        {#each contactInformation as person}
            <p>
                {person.navn}: {person.telefon} / <a href="mailto:{person.epost}">{person.epost}</a>
            </p>
        {/each}
    </details>
    <h2>Vielse 💍</h2>
    <p>
        Vielsen vil finne sted på gården kl 14.00. Tatt geografien i betraktning bør man være forbedret på vær og vind. Paraply kan være et godt supplement til kjole, dress eller bunad.
    </p>
    <p>
        Mellom vielse og middag vil det bli fototgrafering av brudeparet. For gjestene serveres det i dette tidsrommet velkomstdrink og kanapé. Dette er en fin anledning til å ta inn den vakre atmosfæren på gården, hilse på dyrene og mingle med andre gjester. Trolig vil det være mulighet å bedrive små aktiviteter som kubb og boccia.
    </p>
    <details>
        <summary><span class="summary-title">Bilder</span></summary>
        <p>
            Det vil være fotograf tilstede under vielsen og det vil skje noe fotografering mellom vielsen og middagsselskapet. Dersom du tar noen bilder under dagen, blir vi svært glade om du vil dele det med oss i etterkant.
        </p>
        <p style="font-style: italic">Lenke til bildedeling kommer</p>
    </details>
    <h2>Selskap 🎉</h2>
    <p>
        Middagsselskap og bryllupsfest vil være i låven på gården. Det serveres en treretters middag med drikkepakke. Informasjon om meny kommer etterhvert. Etter middag vil det være mulig å kjøpe ytterligere drikke i baren. Samtidig som kakebordet vil fylles av lekre verk. Nattmat skal dere selvfølgelig få!
    </p>
    <details>
        <summary><span class="summary-title">Allergier og preferanser</span></summary>
        <p>
            Dersom noen har allergier, bes det om tilbakemelding om dette til Frid skriftlig (se kontaktinformasjon). Alkoholfri drikkepakke er et alternativ dersom det er ønskelig. Også dette vil vi gjerne ha tilbakemelding på fortløpende. Senest 15.04.24.
        </p>
    </details>
    <details>
        <summary><span class="summary-title">Vil du bidra med noe?</span></summary>
        <p>
            Ønsker du å bake en kake? Ta i så fall kontakt med {baker.navn} på tlf. {baker.telefon}.
            Kaker kan leveres direkte til Kvitnes gård dagen før eller så kjører {baker.navn} til Kvitnes fredag kl. {baker.kjoretidspunkt} for å sette kaker i kjøla, og kan ta med flere.
        </p>
    </details>
    <h2>Kvitnes gård</h2>
    <picture>
        <source srcset="kvitnes.webp" type="image/webp">
        <source srcset="kvitnes.jpg" type="image/jpg">
        <img src="kvitnes.jpg" alt="Hovedbygget på Kvitnes gård i grønne omgivelser, og en blå sommerhimmel i bakgrunnen" />
    </picture>
    <p class="caption">Kvitnes gård en sommerdag i 2021. Foto: <a href="https://hannajohre.com/#about-me" target="_blank">Hanna Johre</a></p>
    <p>Kvitnes Gård er den nyrenoverte gamle storgården i Hadsel i Vesterålen. I dag drives det som et gårdshotell med en av Norges beste restauranter og som et nordlig eksempel på regenerativt jordbruk. Råvarene som brukes i matlagingen dyrkes på gården eller kommer fra nærområdet.</p>
    <a href="https://www.kvitnes.com/" target="_blank">Les mer på kvitnes.no</a>
    <h2>Reise/transport 🚗</h2>
    <p>
        Kvitnes gård ligger en 45 minutters kjøretur fra Sortland. Det er ikke satt opp noe organisert transport. Gjester oppfordres til å organisere dette selv.
    </p>
    <h2>Overnatting 🛏️</h2>
    <p>
        Det er totalt 15 rom med mulighet for overnatting på gården. Først vil nærmeste familie tilbys muligheten å bo på disse rommene, men dersom flere rom er ledig vil enkelte gjester også få mulighet til dette. Dersom dette er noe du/dere kunne tenke deg/dere, bare ta kontakt med oss, så skal vi si fra dersom det står rom ledig.
    </p>
    <p>
        Ut over dette er det to hoteller på Sortland (Scandic og Thon) som begge varmt anbefales.
    </p>
    <h2>Ønskeliste</h2>
    <p>
        Vi synes det er stor stas at folk tar seg tid og råd til å delta i vår kjærlighetsfest.  Om du ønsker å gi oss en bryllupsgave så er det selvfølgelig mulig.
    </p>
    <p style="font-style: italic">Ønskeliste kommer senere</p>
</main>

<style>
    main {
        max-width: 490px;
        border-radius: 1rem;
        margin: 0.5rem;
        background-color: white;
        padding: 1.25rem;
        font-size: 18px;
    }
    h1 {
        text-align: center;
    }
    @media screen and (min-width: 34rem) {
        main {
            margin: 1rem auto;
        }
    }
    img {
        width: 100%;
    }
    details {
        border: solid 1px #aaa;
        border-radius: 4px;
        box-shadow: 0 2px 5px gray;
        margin-top: 0.5rem;
    }
    details > p {
        margin: 0.5rem;
    }
    summary {
        text-align: start;
        padding: 0.5rem;
        border-bottom: 1px solid #aaa;
    }
    .summary-title {
        font-weight: bold;
    }
    .caption {
        font-style: italic;
        text-align: center;
        margin-top: 0;
    }
    iframe {
        max-width: 100% !important;
    }
</style>


