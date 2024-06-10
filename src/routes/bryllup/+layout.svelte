<svelte:head>
	<title>Frid og Larus' bryllup</title>
</svelte:head>

<section>
	<h1>Frid og Larus' bryllup</h1>
	<p style="text-align: center">Vi gifter oss 15. juni 2024!</p>
	<picture>
		<source srcset="/frid-og-larus.webp" type="image/webp">
		<source srcset="/frid-og-larus.jpg" type="image/jpg">
		<img src="/frid-og-larus.jpg" alt="Smilende Frid og noe ukomfortabel Larus" />
	</picture>
	<slot />
</section>

<style>
    h1 {
        text-align: center;
    }
		img {
			width: 100%;
		}
</style>