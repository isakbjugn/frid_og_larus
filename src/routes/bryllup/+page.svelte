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
</script>

<section>
	<p class="note">Den opprinnelige invitasjonen finnes på <a href="/bryllup/invitasjon">/bryllup/invitasjon</a>.</p>
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
</section>

<style>
    .note {
        font-style: italic;
        text-align: center;
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
</style>


