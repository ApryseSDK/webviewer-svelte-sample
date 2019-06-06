<script>

	import { onMount, createEventDispatcher } from 'svelte';

  let instance = null;
  const dispatch = createEventDispatcher();

	onMount(async () => {
		const ele = document.getElementById('viewer');
		const viewer = new window.PDFTron.WebViewer({
      path: '/lib'
		}, ele);

		ele.addEventListener('ready', () => {
      instance = viewer.getInstance();
      dispatch('ready', {
        instance
      })
		})
	});

</script>

<style>
	#viewer {
		width: 100%;
		height: 100%;
	}
</style>


<div id='viewer'>

</div>