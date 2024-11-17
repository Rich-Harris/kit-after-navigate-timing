<script>
	import { afterNavigate } from '$app/navigation';
	import { page } from '$app/stores';
	import { fade } from 'svelte/transition';

	const id = $page.route.id;

	afterNavigate(({ from, to }) => {
		console.log(`${from?.url.pathname} -> ${to?.url.pathname}`);

		if (from?.route.id === id) {
			console.error('this should not run');
		}
	});
</script>

<h1 transition:fade={{ duration: 1 }}>with-transition</h1>
