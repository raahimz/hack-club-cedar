<script>
	import '../app.css';
	import Navbar from '../components/Navbar/Navbar.svelte';
	import Background from '../components/Background.svelte';
</script>

<div class="absolute inset-0 z-[-10]">
	<Background />
</div>

<Navbar />
<div class="py-2">
	<slot />
</div>
