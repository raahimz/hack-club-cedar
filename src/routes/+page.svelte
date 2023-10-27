<script>
	import Header from '../components/sections/header/Header.svelte';
	import Introduction from '../components/sections/introduction/Introduction.svelte';
	import Socials from '../components/sections/socials/Socials.svelte';
	import Container from '../components/sections/credits/Container.svelte';
	import { Masonry } from 'svelte-bricks';
	import Person from '../components/sections/credits/Person.svelte';

	// Masonry values
	let [minColWidth, maxColWidth, gap] = [230, 230, 10];

	const executives = [
		{
			id: 1,
			name: 'Ali Hussain',
			work: 'President',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},
		{
			id: 2,
			name: 'Ameen Abbasi',
			work: 'Vice President',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},
		{
			id: 3,
			name: 'Minhaal Jamil',
			work: 'Vice President',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},

		{
			id: 4,
			name: 'Shaheer',
			work: 'Project Manager',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},
		{
			id: 5,
			name: 'Hatim Mustufa',
			work: 'Project Manager',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},
		{
			id: 6,
			name: 'Murtuza',
			work: 'Project Manager',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},

		{
			id: 7,
			name: 'Raahim Zeeshan',
			work: 'Web Dev Head',
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
			id: 8,
			name: 'Abbad',
			work: 'Graphic Design Head',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},
		{
			id: 9,
			name: 'Saif Ahmed',
			work: 'Promotion Head',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		},
		{
			id: 10,
			name: 'Abbas',
			work: 'AI Head',
			imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
			socials: [
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' },
				{ network: 'email', url: 'https://www.google.com' }
			]
		}
	];
</script>

<main>
	<div class="h-[80vh] flex justify-center pt-[27vh]">
		<Header />
	</div>
	<Socials />
	<Introduction />
	<div class="flex flex-col gap-2 mt-12">
		<div class="w-fit self-center">
			<Container><p class="text-teal-500 font-bold text-xl">Executives</p></Container>
		</div>
		<Masonry items={executives} {minColWidth} {maxColWidth} {gap} let:item>
			<Person name={item.name} work={item.work} socials={item.socials} imageURL={item.imageURL} />
		</Masonry>
	</div>
</main>
