<script lang="ts">
	import type { Snippet } from "svelte";

  type Props = {
    title: string;
    description: string;
    icon: Snippet;
  };

  let { icon, title, description }: Props = $props();
</script>

<div class="card  bg-surface-50 dark:bg-surface-950 p-8 flex flex-col items-center text-center rounded-lg shadow-md" >
  <div class="w-16 h-16 mb-4 rounded-full flex items-center justify-center bg-primary-400">
    <div class="w-8 h-8 text-surface-800 dark:text-surface-950 " >  
      {@render icon()} 
    </div>
  </div>
  <div class="h3 mb-2">{title}</div>
  <p class="text-surface-500-400-token mb-2 py-1 text-justify">{description}</p>
</div>