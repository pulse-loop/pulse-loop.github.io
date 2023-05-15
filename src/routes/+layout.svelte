<script>
	import '../app.css';
</script>

<!-- Vertical sidebar -->
<nav class="invisible fixed bottom-0 mix-blend-multiply md:visible">
	<img
		src="logos/pl_text.svg"
		alt="pulse.loop logo"
		class="-z-10 h-16 origin-bottom-left translate-x-16 -rotate-90"
	/>
</nav>

<nav class="visible z-50 flex w-screen flex-row justify-around bg-white md:invisible">
	<img src="logos/pl.png" alt="pulse.loop logo" class="h-16 p-5" />
</nav>

<div>
	<main class="flex flex-col overflow-x-hidden">
		<slot />
	</main>
</div>
