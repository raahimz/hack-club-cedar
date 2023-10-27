<script>
	import Container from '../credits/Container.svelte';
	import Carousel from 'svelte-carousel/src/components/Carousel/Carousel.svelte';
	import { browser } from '$app/environment';
	import Winner from './Winner.svelte';
	import { Masonry } from 'svelte-bricks';

	export let title;
	export let description;
	export let winners;
	export let department;
	export let images;

	// Masonry values
	let [minColWidth, maxColWidth, gap] = [170, 170, 10];

	let carousel; // for calling methods of the carousel instance

	const handleNextClick = () => {
		carousel.goToNext();
	};
</script>

<Container>
	<div class="flex flex-col justify-center items-center">
		<h3 class="font-bold text-teal-500 text-xl">{title}</h3>
		<p class="font-bold">{department}</p>
		<p class="mt-2 font-light">{description}</p>

		{#if browser}
			<div class="max-w-xs flex flex-col gap-2 mt-4">
				<Carousel bind:this={carousel} autoplay={true} autoplayProgressVisible={true}>
					{#each images as image}
						<img
							class="rounded-md border-[1px] border-gray-800 shadow-sm"
							src={image}
							alt={`image'`}
							width="200"
						/>
					{/each}
				</Carousel>
			</div>
		{/if}
	</div>
	{#if winners.length > 0}
		<div class="border-gray-700 rounded-md border-[1px] p-2">
			<p class="font-bold uppercase mb-2 text-teal-600 text-xl">Winners</p>
			<Masonry items={winners} {minColWidth} {maxColWidth} {gap} let:item>
				<Winner name={item.name} imageURL={item.imageURL} />
			</Masonry>
		</div>
	{/if}
</Container>
