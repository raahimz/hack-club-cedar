<script>
	import Container from '../../components/sections/credits/Container.svelte';
	import Person from '../../components/sections/credits/Person.svelte';
	import Title from '../../components/sections/credits/Title.svelte';
	import Masonry from 'svelte-bricks';

	// Masonry values
	let [minColWidth, maxColWidth, gap] = [230, 230, 10];

	const creators = [
		{
			id: 1,
			name: 'Raahim Zeeshan',
			work: 'Developer',
			imageURL: 'https://avatars.githubusercontent.com/u/81946686?v=4',
			socials: [
				{
					url: 'https://github.com/raahimz',
					network: 'github'
				},
				{
					url: 'https://www.instagram.com/raahimzee',
					network: 'instagram'
				},
				{
					url: 'https://www.linkedin.com/in/raahim-zeeshan-276827162/',
					network: 'linkedin'
				}
			]
		},
		{
			id: 2,
			name: 'Shivam Kumar',
			work: 'QA Tester',
			imageURL: 'https://avatars.githubusercontent.com/u/123737956?v=4',
			socials: [
				{
					url: 'https://github.com/HaZeRubyYT',
					network: 'github'
				},
				{
					url: 'https://www.instagram.com/shivam.khatri.96/',
					network: 'instagram'
				},
				{
					url: 'https://x.com820shivamkumart=V-exXFgOFtzV2uvER0ModA&s=09',
					network: 'twitter'
				}
			]
		},
		{
			id: 3,
			name: 'Awab Saghir',
			work: 'QA Tester',
			imageURL: 'https://avatars.githubusercontent.com/u/125585883?v=4',
			socials: [
				{
					url: 'https://github.com/xAwabx',
					network: 'github'
				},
				{
					url: 'https://www.instagram.com/awab_ghouri/',
					network: 'instagram'
				},
				{
					url: 'https://www.linkedin.com/in/awab-saghir-a8a1a7245/',
					network: 'linkedin'
				}
			]
		}
	];
</script>

<main class="mt-8 flex flex-col gap-6 pt-8">
	<div class="w-fit self-center">
		<Title>Credits</Title>
	</div>
	<div class="flex flex-col gap-2">
		<div class="w-fit self-center">
			<Container
				><p class="text-teal-500 font-bold text-xl">This website was made with ❤️ by</p></Container
			>
		</div>
		<Masonry items={creators} {minColWidth} {maxColWidth} {gap} let:item>
			<Person name={item.name} work={item.work} socials={item.socials} imageURL={item.imageURL} />
		</Masonry>
	</div>
</main>
