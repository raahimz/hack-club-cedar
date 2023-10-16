<script>
	import Header from '../components/sections/header/Header.svelte';
	import Introduction from '../components/sections/introduction/Introduction.svelte';
	import Socials from '../components/sections/socials/Socials.svelte';
</script>

<main>
	<div class="mt-[25vh]">
		<Header />
	</div>
	<div class=" mt-[40vh] flex flex-col w-full gap-2">
		<Socials />
		<Introduction />
	</div>
</main>
