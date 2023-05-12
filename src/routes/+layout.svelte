<script>
	import '../app.css';
</script>

<!-- Vertical sidebar -->
<nav class="fixed bottom-0 mix-blend-multiply">
	<!-- Padding -->
	<img
		src="logo.svg"
		alt="pulse.loop logo"
		class="-z-10 h-16 origin-bottom-left translate-x-16 -rotate-90"
	/>
</nav>

<div>
	<main class="flex flex-col overflow-x-hidden">
		<slot />
	</main>
</div>
