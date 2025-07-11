<script lang="ts">
	import type { Snippet } from "svelte";

  type Props = {
    title: string;
    description: string;
    icon: Snippet;
    class?: string;
  };

  let { icon, title, description, class: className = "" }: Props = $props();
</script>

<div class="card p-8 flex flex-col items-center text-center rounded-2xl shadow-lg hover:shadow-xl transition-all duration-300 {className}">
  <div class="mb-6">
    {@render icon()} 
  </div>
  <h3 class="text-xl font-bold text-surface-900 mb-4 leading-tight">{title}</h3>
  <p class="text-surface-600 leading-relaxed">{description}</p>
</div>