<main>
	<slot />
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
    @media screen and (min-width: 34rem) {
        main {
            margin: 1rem auto;
        }
    }
</style>


