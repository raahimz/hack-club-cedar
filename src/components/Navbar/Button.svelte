<script>
	import { goto } from '$app/navigation';
	export let url;

	const onClickHandler = () => {
		goto(url);
	};
</script>

<button on:click={onClickHandler}>
	<p class="hover:opacity-80 font-mono hover:underline">
		<slot />
	</p>
</button>
