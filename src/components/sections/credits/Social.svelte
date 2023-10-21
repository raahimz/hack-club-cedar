<script>
	import SocialIcons from '@rodneylab/svelte-social-icons';
	export let url;
	export let network;
</script>

<a href={url} target="_blank" class="hover:opacity-80 active:opacity-80">
	<SocialIcons {network} width="42" height="42" bgColor="#000000" fgColor="#ffffff" />
</a>
