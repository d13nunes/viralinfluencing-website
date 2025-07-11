<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<div class="h-screen w-screen overflow-y-auto bg-amber-50">
	{@render children()}
</div>
