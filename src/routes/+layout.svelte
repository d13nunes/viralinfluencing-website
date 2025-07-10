<script lang="ts">
	import '../app.css';
	import MailingListForm from '$lib/MailingListForm.svelte';

	let { children } = $props();
</script>

<div class="w-screen h-screen overflow-y-auto  bg-gradient-to-br from-surface-50 to-surface-200 dark:from-surface-700 dark:to-surface-600 pb-16">
		{@render children()}
</div>