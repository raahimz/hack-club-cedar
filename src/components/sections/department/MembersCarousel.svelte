<script>
	export let members;
	import Person from '../credits/Person.svelte';
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import Container from '../credits/Container.svelte';
	import Title from '../credits/Title.svelte';

	let carousel; // for calling methods of the carousel instance

	const handleNextClick = () => {
		carousel.goToNext();
	};
</script>

{#if browser}
	<div class="max-w-sm flex flex-col gap-2">
		<Carousel bind:this={carousel} autoplay={true} autoplayProgressVisible={true}>
			{#each members as member}
				<div class="max-w-[32px]">
					<Person
						name={member.name}
						work={member.work}
						socials={member.socials}
						imageURL={member.imageURL}
					/>
				</div>
			{/each}
		</Carousel>
	</div>
{/if}
