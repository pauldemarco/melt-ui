<script lang="ts">
	import { createTooltip, melt } from '$lib/index.js';
	import { fade } from 'svelte/transition';
	import { Plus } from 'lucide-svelte';
	import ListTile from './ListTile.svelte'

	const items = Array.from(Array(5), (_, index) => index);

</script>

<div class="w-full flex flex-col gap-2">
    {#each items as item}
    <ListTile title={item} />
    {/each}
  </div>

<style lang="postcss">
	.trigger {
		@apply inline-flex h-9 w-9 items-center justify-center rounded-full bg-white;
		@apply text-magnum-900 transition-colors hover:bg-white/90;
		@apply focus-visible:ring focus-visible:ring-magnum-400 focus-visible:ring-offset-2;
		@apply p-0 text-sm font-medium;
	}
</style>
