<script>
	import Postcard from '$lib/Postcard.svelte';

	let cardShown = $state(false);
</script>

{#snippet heading()}
	<h1>Hello World</h1>
{/snippet}
{#snippet content()}
	<p>This is nice</p>
{/snippet}

<button class="bg-blue-400" onclick={() => (cardShown = !cardShown)}>Show card</button>
{#if cardShown}
	<Postcard {heading} {content} />
{/if}
