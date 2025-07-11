<script lang="ts">
	import type { Snippet } from 'svelte';

	type Props = {
		title: string;
		description: string;
		icon: Snippet;
		class?: string;
	};

	let { icon, title, description, class: className = '' }: Props = $props();
</script>

<div
	class="card flex flex-col items-center rounded-2xl p-8 text-center shadow-lg transition-all duration-300 hover:shadow-xl {className}"
>
	<div class="mb-6">
		{@render icon()}
	</div>
	<h3 class="text-surface-900 mb-4 text-xl leading-tight font-bold">{title}</h3>
	<p class="text-surface-600 leading-relaxed">{description}</p>
</div>
