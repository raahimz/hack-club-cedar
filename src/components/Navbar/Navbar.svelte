<script>
	import Button from './Button.svelte';
</script>

<div
	class="flex flex-row gap-2 bg-black items-center justify-between blur-filter p-4 border-[1px] border-gray-900 bg-opacity-20 mx-4 sticky top-2 rounded-lg shadow-sm"
>
	<div>
		<Button url={'/'}><span class="font-extrabold">HACK CLUB</span></Button>
	</div>
	<div class="flex flex-row gap-6">
		<Button url={'/web-dev'}>WEB DEV</Button>
		<p>•</p>
		<Button url={'/esports'}>E SPORTS</Button>
	</div>
</div>

<style>
	.blur-filter {
		-webkit-backdrop-filter: blur(3px);
		backdrop-filter: blur(3px);
	}
</style>
