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

<main class="mt-8 flex flex-col gap-6 pt-8">
	<div class="w-fit self-center">
		<Title>Credits</Title>
	</div>

	<div class="flex flex-col gap-2">
		<div class="w-fit self-center">
			<Container>This website was made with ❤️ by</Container>
		</div>
		<Masonry items={creators} {minColWidth} {maxColWidth} {gap} let:item>
			<Person name={item.name} work={item.work} socials={item.socials} imageURL={item.imageURL} />
		</Masonry>
	</div>

	<div class="flex flex-col gap-2">
		<div class="w-fit self-center">
			<Container>Hack Club Executives</Container>
		</div>
		<Masonry items={executives} {minColWidth} {maxColWidth} {gap} let:item>
			<Person name={item.name} work={item.work} socials={item.socials} imageURL={item.imageURL} />
		</Masonry>
	</div>
</main>
