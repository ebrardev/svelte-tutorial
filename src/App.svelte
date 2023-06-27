<script>
	import LogoText from './LogoText.svelte';
	import Counter from './Counter.svelte';
	import Auth from './Auth.svelte';
	export let name;
	export let surname
</script>

<LogoText comp="svelte" />
<Auth />
<Counter />
<br> <br>
<main>
	<h1>Hello {name}!</h1>
	<h1> {surname}</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>


<style lang="scss" >
	@import "styles/variables";
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: $color;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>