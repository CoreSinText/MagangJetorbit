<script>
	import '../app.css';
	import Navbar from './Navbar.svelte';
</script>

<div class="w-screen">
	<Navbar />

	<main class="w-screen">
		<slot />
	</main>
</div>
