<script>
	import Kvitnes from '$lib/components/Kvitnes.svelte';

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
	const baker = brud;
	const contactInformation = [brud, brudgom, kjokemester]
	const lastRegistrationDate = new Date('2024-04-15');
	const accountNumber = '4612 15 32492';

	function formatDate(date) {
		return date.toLocaleDateString('nb-NO', {
			day: 'numeric',
			month: 'long',
			year: 'numeric',
		});
	}

	function isRegistrationOpen() {
		const today = new Date();
		return today < new Date(lastRegistrationDate.getDate() + 1)
	}
</script>

<section>
	<p>
		Vi er utrolig takknemlig og kry over at så mange ønsker å komme til Vesterålen for å feire kjærligheten vår. Valget vårt for sted til bryllup falt på Kvitnes gård etter å ha opplevd atmosfæren på gården ved et besøk dit vinteren 2022, samt etter flere middager på Lille Kvitnes på Sortland. Vårt ønske er å få dele et særdeles godt måltid og tilbringe tid sammen med de vi er glade i.
	</p>
	<details>
		<summary><span class="summary-title">Registrering</span></summary>
		{#if isRegistrationOpen()}
			<iframe
				title="Gjesteregistrering (skjema)"
				src="https://docs.google.com/forms/d/e/1FAIpQLSf4K5RrZjA3-oifJuFVl5HVP-TykvU1thDPJR03Y5pGY8YxjA/viewform?embedded=true"
				width="488"
				height="704"
				frameborder="0"
				marginheight="0"
				marginwidth="0"
			/>
		{:else}
			<p>
				Registreringen var åpen til {formatDate(lastRegistrationDate)}, og er nå stengt. Dersom du har spørsmål, ta kontakt med oss på e-post eller telefon.
			</p>
		{/if}
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
		Mellom vielse og middag vil det bli fotografering av brudeparet. For gjestene serveres det i dette tidsrommet velkomstdrink og kanapé. Dette er en fin anledning til å ta inn den vakre atmosfæren på gården, hilse på dyrene og mingle med andre gjester. Trolig vil det være mulighet å bedrive små aktiviteter som kubb og boccia.
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
			Dersom noen har allergier, bes det om tilbakemelding om dette til Frid skriftlig (se kontaktinformasjon). Alkoholfri drikkepakke er et alternativ dersom det er ønskelig. Også dette vil vi gjerne ha tilbakemelding på fortløpende. Senest {formatDate(lastRegistrationDate)}.
		</p>
	</details>
	<details>
		<summary><span class="summary-title">Vil du bidra med noe?</span></summary>
		<p>
			Ønsker du å bake en kake? Ta i så fall kontakt med {baker.navn} på tlf. {baker.telefon}.
			Kaker kan leveres direkte til Kvitnes gård dagen før eller så kjører {baker.navn} til Kvitnes fredag formiddag for å sette kaker i kjøla, og kan ta med flere.
		</p>
	</details>
	<Kvitnes />
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
		Vi synes det er stor stas at folk tar seg tid og råd til å delta i vår kjærlighetsfest. Om du ønsker å gi oss en bryllupsgave, så har vi laget en ønskeliste hos <span style="font-style: italic">Kitch'n</span>:
	</p>
	<a href="https://www.kitchn.no/onskeliste/173519/">https://www.kitchn.no/onskeliste/173519/</a>
	<p>Vi blir også glade for pengegaver som øremerkes bildekunst til vårt hjem. Disse kan settes inn på kontonummer {accountNumber}.</p>
</section>

<style>
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
    iframe {
        max-width: 100% !important;
    }
</style>


