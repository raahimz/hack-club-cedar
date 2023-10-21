<script>
	import InfoContainer from '../../../components/sections/introduction/InfoContainer.svelte';
	import Title from '../../../components/sections/credits/Title.svelte';
	import Person from '../../../components/sections/credits/Person.svelte';
	import MembersCarousel from '../../../components/sections/department/MembersCarousel.svelte';

	const members = [
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
		<Title>Lorem Ipsum</Title>
	</div>
	<div class="flex flex-col gap-3">
		<InfoContainer
			title={'NULLA EMIT SUSCIPIT'}
			description={'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Aliquid dolorum natus maiores quod totam nisi nemo expedita ut suscipit modi molestiae nulla exercitationem minima deserunt, corporis cumque vel dolorem optio!'}
		/>
		<InfoContainer
			title={'ROLET MODI OPTIO'}
			description={'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet blanditiis iste obcaecati impedit, ex ratione? Voluptates hic delectus neque cumque officia ex accusantium reprehenderit deleniti aperiam enim. Aliquam, quod quis.'}
		/><InfoContainer
			title={'CUMQUE VEL DOLOREM'}
			description={'Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium similique molestiae doloribus ipsum quasi blanditiis suscipit explicabo facilis, maxime laborum natus culpa, officia, illo excepturi enim corrupti repudiandae. Explicabo, harum.'}
		/>
	</div>
	<MembersCarousel {members} />
</main>
