<script>
	import '../app.css';
</script>

<!-- Vertical sidebar -->
<nav
	class="fixed bottom-0 mix-blend-multiply"
>
	<!-- Padding -->
	<img src="logo.svg" alt="pulse.loop logo" class="h-16 -rotate-90 origin-bottom-left translate-x-16" />
</nav>

<div>
	<main class="flex flex-col">
		<slot />
	</main>
</div>
