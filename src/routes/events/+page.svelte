<script>
	import Title from '../../components/sections/credits/Title.svelte';
	import Container from '../../components/sections/credits/Container.svelte';
	import Person from '../../components/sections/credits/Person.svelte';
	import Masonry from 'svelte-bricks';
	import Event from '../../components/sections/events/Event.svelte';

	// Masonry values
	let [minColWidth, maxColWidth, gap] = [500, 500, 10];

	const events = {
		ongoing: [
			{
				id: 1,
				title: 'Lorem Ipsum',
				description:
					'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem fuga officiis saepe incidunt deleniti eum quasi eveniet totam itaque ab harum, id dolore odit ipsum, possimus deserunt accusantium quaerat? Officia?',
				department: 'Web Dev',
				winners: [],
				images: [
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
				]
			},
			{
				id: 2,
				title: 'Lorem Ipsum',
				description:
					'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Autem fuga officiis saepe incidunt deleniti eum quasi eveniet totam itaque ab harum, id dolore odit ipsum, possimus deserunt accusantium quaerat? Officia?',
				department: 'Web Dev',
				winners: [],
				images: [
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
				]
			}
		],
		completed: [
			{
				id: 1,
				title: 'Dolor Emet',
				description:
					'Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias doloremque mollitia molestias, voluptates ad praesentium exercitationem aperiam eius, excepturi consectetur, incidunt libero placeat fuga provident quae quis voluptatum officiis ea.    ',
				department: 'Graphic Design',
				winners: [
					{
						id: 1,
						name: 'Asad Faraz',
						imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
					},
					{
						id: 2,
						name: 'Asad Faraz',
						imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
					}
				],
				images: [
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
				]
			},
			{
				id: 2,
				title: 'Dolor Emet',
				description:
					'Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias doloremque mollitia molestias, voluptates ad praesentium exercitationem aperiam eius, excepturi consectetur, incidunt libero placeat fuga provident quae quis voluptatum officiis ea.    ',
				department: 'Graphic Design',
				winners: [
					{
						id: 1,
						name: 'Asad Faraz',
						imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
					},
					{
						id: 2,
						name: 'Asad Faraz',
						imageURL: 'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
					}
				],
				images: [
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png',
					'https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png'
				]
			}
		]
	};
</script>

<main class="mt-8 flex flex-col justify-center items-center gap-8 mb-4">
	<div class="w-fit">
		<Title>EVENTS</Title>
	</div>
</main>

<div
	class="relative border-gray-800 rounded-md border-[1px] px-4 pb-4 mt-10 bg-black bg-opacity-20"
>
	<div class="flex flex-col gap-2 absolute left-1/2 transform -translate-x-1/2 -translate-y-1/2">
		<div class="w-fit self-center mb-2">
			<Container>ONGOING</Container>
		</div>
	</div>

	<div class="mt-8">
		<Masonry items={events.ongoing} {minColWidth} {maxColWidth} {gap} let:item>
			<Event
				title={item.title}
				description={item.description}
				winners={item.winners}
				department={item.department}
				images={item.images}
			/>
		</Masonry>
	</div>
</div>

<div
	class="relative border-gray-800 rounded-md border-[1px] px-4 pb-4 mt-10 bg-black bg-opacity-20"
>
	<div class="flex flex-col gap-2 absolute left-1/2 transform -translate-x-1/2 -translate-y-1/2">
		<div class="w-fit self-center mb-2">
			<Container>COMPLETED</Container>
		</div>
	</div>
	<div class="mt-8">
		<Masonry items={events.completed} {minColWidth} {maxColWidth} {gap} let:item>
			<Event
				title={item.title}
				description={item.description}
				winners={item.winners}
				department={item.department}
				images={item.images}
			/>
		</Masonry>
	</div>
</div>

<style>
	.blur-filter {
		-webkit-backdrop-filter: blur(3px);
		backdrop-filter: blur(3px);
	}
</style>
