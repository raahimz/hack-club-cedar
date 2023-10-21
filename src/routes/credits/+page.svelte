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
					url: 'https://google.com',
					network: 'github'
				},
				{
					url: 'https://google.com',
					network: 'instagram'
				},
				{
					url: 'https://google.com',
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
					url: 'https://google.com',
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
		<Container>This website was made with ❤️ by</Container>
		<div class="flex flex-row gap-2 items-center justify-center">
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
