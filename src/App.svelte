<script>

	import { onMount } from 'svelte';

	onMount(async () => {
		const ele = document.getElementById('viewer');
		const viewer = new window.PDFTron.WebViewer({
			path: '/lib'
		}, ele);

		ele.addEventListener('ready', () => {
			const instance = viewer.getInstance();
			// user webviewer APIs here!
		})
	})
</script>

<style>
	#viewer {
		width: 100%;
		height: 100%;
	}
</style>


<div id='viewer'>

</div>

