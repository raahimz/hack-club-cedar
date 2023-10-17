<script>
	export let title;
	export let description;
</script>

<div
	class="flex flex-col gap-2 bg-black items-center justify-center p-6 bg-opacity-75 w-[90%] ml-auto mr-auto rounded-lg shadow-sm border-[1px] border-gray-800"
>
	<h1 class="text-3xl font-mono text-teal-500">{title}</h1>
	<p class="max-w-2xl text-center font-sans">
		{description}
	</p>
</div>

<style>
	.blur-filter {
		-webkit-backdrop-filter: blur(3px);
		backdrop-filter: blur(3px);
	}
</style>
