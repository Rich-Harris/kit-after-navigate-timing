<script>
	let { children } = $props();
</script>

<nav>
	<a href="/">home</a>
	<a href="/with-transition">with-transition</a>
	<a href="/without-transition">without-transition</a>
</nav>

{@render children()}
