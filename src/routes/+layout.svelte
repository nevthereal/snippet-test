<script>
	import { toast, Toaster } from 'svelte-sonner';
	import '../app.css';

	let { children } = $props();
</script>

<Toaster
	toastOptions={{
		unstyled: true
	}}
/>
<button onclick={() => toast('yay')}>Yay</button>
{@render children()}
