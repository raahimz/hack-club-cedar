<script>
	import '../app.css';
	import Navbar from '../components/Navbar/Navbar.svelte';
	import Background from '../components/Background.svelte';
</script>

<div class="absolute inset-0 z-[-10]">
	<Background />
</div>

<div class="top-2 sticky z-10">
	<Navbar />
</div>
<div class="py-2 px-4">
	<slot />
</div>
