<script lang="ts">
	import './services/i18n/i18n';
	import {
		_,
		isLoading,
	} from 'svelte-i18n';
	import Section from './components/landing/section.svelte';
</script>

{#if $isLoading}
	Please wait...
{:else}
	<main>
		<h1>Hello {$_('username')}!</h1>
		<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
		<Section>
			<h2>Label</h2>
		</Section>
		<Section>
			<h2>Label</h2>
		</Section>
	</main>
{/if}

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
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