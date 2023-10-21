<div
	class="bg-black bg-opacity-40 shadow-sm border-[1px] border-gray-800 w-full p-4 rounded-md blur-filter text-center font-mono uppercase"
>
	<slot />
</div>

<style>
	.blur-filter {
		-webkit-backdrop-filter: blur(3px);
		backdrop-filter: blur(3px);
	}
</style>
