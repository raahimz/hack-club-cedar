<script>
	import Container from '../../components/sections/credits/Container.svelte';
	import Person from '../../components/sections/credits/Person.svelte';
	import Title from '../../components/sections/credits/Title.svelte';

	const people = [
		{
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

<main class="mt-8 flex flex-col justify-center items-center gap-8">
	<div class="w-fit">
		<Title>Credits</Title>
	</div>
	<div class="flex-col flex items-center justify-center gap-2">
		<div class="max-w-[250px] md:max-w-none w-fit md:w-full">
			<Container>This website was made with ❤️ by</Container>
		</div>
		<div class="flex flex-col md:flex-row gap-2 items-center justify-center">
			{#each people as person}
				<Person
					name={person.name}
					work={person.work}
					socials={person.socials}
					imageURL={person.imageURL}
				/>
			{/each}
		</div>
	</div>
</main>
