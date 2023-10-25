<script>
	import Button from './Button.svelte';
	import Dropdown from './Dropdown.svelte';
	import HamburgerIcon from './HamburgerIcon.svelte';

	let showHamburgerMenu = false;
	let showDropdown = false;
</script>

<div
	class=" bg-black p-4 border-[1px] border-gray-800 bg-opacity-30 mx-4 rounded-lg shadow-sm z-10 blur-filter"
>
	<div class="hidden sm:flex flex-row gap-2 justify-between items-center">
		<div>
			<Button url={'/'}><span class="font-extrabold">HACK CLUB</span></Button>
		</div>
		<div class="flex flex-row gap-6">
			<!-- svelte-ignore a11y-no-static-element-interactions -->
			<!-- svelte-ignore a11y-mouse-events-have-key-events -->
			<div on:mouseover={() => (showDropdown = true)} on:mouseleave={() => (showDropdown = false)}>
				<p class="font-mono hover:cursor-pointer">DEPARTMENTS</p>
				<div class="absolute">
					{#if showDropdown}
						<Dropdown />
					{/if}
				</div>
			</div>
			<p>•</p>
			<Button url={'/credits'}>CREDITS</Button>
			<p>•</p>
			<Button url={'/events'}>EVENTS</Button>
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
			<Button url={'/credits'}>CREDITS</Button>
			<Button url={'/events'}>EVENTS</Button>
			<div class="text-center py-2 flex flex-row items-center justify-center gap-4">
				<div class="h-[1px] w-full bg-teal-400 rounded-full" />
				<p class="font-mono text-teal-400">DEPARTMENTS</p>
				<div class="h-[1px] w-full bg-teal-400 rounded-full" />
			</div>
			<Button url={'/departments/webdev'}>WEB DEV</Button>
			<Button url={'/departments/graphic'}>GRAPHIC</Button>
			<Button url={'/departments/ai'}>AI</Button>
		</div>
	{/if}
</div>

<style>
	.blur-filter {
		-webkit-backdrop-filter: blur(3px);
		backdrop-filter: blur(3px);
	}
</style>
