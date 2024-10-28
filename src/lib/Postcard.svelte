<script lang="ts">
	import type { Snippet } from 'svelte';
	import { fly } from 'svelte/transition';

	let { heading, content }: { heading: Snippet; content: Snippet } = $props();
</script>

<div transition:fly class="prose rounded-xl border p-4">
	{@render heading()}
	{@render content()}
</div>
