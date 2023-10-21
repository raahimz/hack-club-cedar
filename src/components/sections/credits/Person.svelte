<script>
	import Socials from '../socials/Socials.svelte';
	import Container from './Container.svelte';
	import Social from './Social.svelte';

	export let name;
	export let work;
	export let socials;
	export let imageURL;
</script>

<Container>
	<div class="flex flex-col justify-center items-center">
		<h3 class="font-bold text-teal-500 text-xl">{name}</h3>
		<p>{work}</p>
		<img
			class="rounded-md border-[1px] border-gray-800 shadow-sm m-2"
			src={imageURL}
			alt={`${name}'s image'`}
			width="200"
		/>

		<div>
			{#each socials as social, index}
				<Social url={social.url} network={social.network} />
			{/each}
		</div>
	</div>
</Container>
