<script>
	import * as THREE from 'three';
	import GLOBE from 'vanta/dist/vanta.globe.min';

	function vanta(node) {
		GLOBE({
			el: node,
			THREE: THREE,
			mouseControls: true,
			touchControls: true,
			gyroControls: false,
			minHeight: 10.0,
			minWidth: 10.0,
			scale: 1,
			scaleMobile: 2,
			color: 0xffc3,
			backgroundColor: 0x121212
		});
	}
</script>

<div class="vanta" use:vanta />

<style>
	.vanta {
		position: fixed;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		z-index: -1;
	}
</style>
