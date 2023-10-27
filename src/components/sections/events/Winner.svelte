<script>
	import Container from '../credits/Container.svelte';

	export let name;
	export let imageURL;
</script>

<Container>
	<div class="flex flex-col justify-center items-center">
		<h3 class="font-bold text-teal-500 text-xl">{name}</h3>
		<img
			class="rounded-md border-[1px] border-gray-800 shadow-sm m-2"
			src={imageURL}
			alt={`${name}'s image'`}
			width="200"
		/>
	</div>
</Container>
