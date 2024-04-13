<script>
	import Header from './Header.svelte';
	import svelte from '$lib/images/svelte-logo.svg';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>made with ♥️ by <a href="https://bcc-nmit-landing.vercel.app/">BCC</a> using</p>
		<a href="https://svelte.dev">
			<img src={svelte} alt="Svelte logo" height="20" />
		</a>
	</footer>
</div>

<style>
	main {
		padding: 1rem;
		margin: 0 auto;
	}
	footer {
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 12px;
		gap: 4px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
	/* .app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	} */
</style>
