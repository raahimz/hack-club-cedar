<script>
	import Button from './Button.svelte';
	import HamburgerIcon from './HamburgerIcon.svelte';

	let showHamburgerMenu = false;
</script>

<div
	class=" bg-black p-4 border-[1px] border-gray-800 bg-opacity-30 mx-4 rounded-lg shadow-sm z-10 blur-filter"
>
	<div class="hidden sm:flex flex-row gap-2 justify-between items-center">
		<div>
			<Button url={'/'}><span class="font-extrabold">HACK CLUB</span></Button>
		</div>

		<div class="flex flex-row gap-6">
			<Button url={'/web-dev'}>WEB DEV</Button>
			<p>•</p>
			<Button url={'/esports'}>E SPORTS</Button>
			<p>•</p>
			<Button url={'/credits'}>CREDITS</Button>
		</div>
	</div>

	<div class="sm:hidden flex flex-row gap-2 justify-between items-center">
		<div>
			<Button url={'/'}><span class="font-extrabold">HACK CLUB</span></Button>
		</div>
		<div class="">
			<button on:click={() => (showHamburgerMenu = !showHamburgerMenu)}>
				<HamburgerIcon />
			</button>
		</div>
	</div>

	{#if showHamburgerMenu}
		<div class="flex flex-col gap-2 pt-5">
			<Button url={'/web-dev'}>WEB DEV</Button>
			<Button url={'/esports'}>E SPORTS</Button>
			<Button url={'/credits'}>CREDITS</Button>
		</div>
	{/if}
</div>

<style>
	.blur-filter {
		-webkit-backdrop-filter: blur(3px);
		backdrop-filter: blur(3px);
	}
</style>
