<script>
	import '../app.css';
</script>

<!-- Vertical sidebar -->
<nav
	class="h-16 rotate-90 origin-top-left translate-x-16 bg-white flex flex-row items-center absolute"
>
	<!-- Padding -->
	<div class="flex-grow" />
	<img src="logo.svg" alt="pulse.loop logo" class="h-16 rotate-180" />
</nav>

<main class="bg-red-50 max-w-6xl px-32">
	<slot />
</main>

<style>
	nav {
		width: 100vh;
	}
</style>
