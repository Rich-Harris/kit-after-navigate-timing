<script>
	import { afterNavigate } from '$app/navigation';
	import { page } from '$app/stores';

	const id = $page.route.id;

	afterNavigate(({ from, to }) => {
		console.log(`${from?.url.pathname} -> ${to?.url.pathname}`);

		if (from?.route.id === id) {
			console.error('this should not run');
		}
	});
</script>

<h1>without-transition</h1>
