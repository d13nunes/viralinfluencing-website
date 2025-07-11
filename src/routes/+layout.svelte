
<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<div class="w-screen h-screen overflow-y-auto bg-amber-50 ">
		{@render children()}
</div>