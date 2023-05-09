<script>
	import '../app.css';
</script>

<!-- Vertical sidebar -->
<nav
	class="h-20 rotate-90 origin-top-left translate-x-20 flex flex-row bg-transparent items-center fixed mix-blend-multiply"
>
	<!-- Padding -->
	<div class="flex-grow" />
	<img src="logo.svg" alt="pulse.loop logo" class="h-16 rotate-180" />
</nav>

<div>
	<main class="flex flex-col">
		<slot />
	</main>
</div>

<style>
	nav {
		width: 100vh;
	}
</style>
