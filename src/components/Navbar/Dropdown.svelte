<script>
	import Container from '../sections/credits/Container.svelte';
	import Button from './Button.svelte';
</script>

<Container>
	<div class="flex flex-col gap-2 px-6">
		<Button url={'/departments/webdev'}>WEB DEV</Button>
		<Button url={'/departments/graphic'}>GRAPHIC</Button>
		<Button url={'/departments/ai'}>AI</Button>
	</div>
</Container>
