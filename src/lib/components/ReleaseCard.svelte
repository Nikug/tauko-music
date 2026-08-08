<script lang="ts">
  import type { Release } from '$lib/types';

  interface Props {
    release: Release;
  }
  const { release }: Props = $props();

  const upcoming = $derived(release.date > new Date());
</script>

<div
  class="min-w-64 shrink rounded border bg-gray-800 px-4 py-2 shadow-blue-800/50 transition-shadow hover:shadow-lg"
>
  <h3 class="text-xl font-bold">{release.name}</h3>
  {#if upcoming}
    <p class="text-sm font-bold text-gray-400">Upcoming</p>
  {/if}
  <p class="text-gray-400">{release.date.toLocaleDateString()}</p>
  <a href={release.link} rel="external" class="text-blue-500 underline">Listen on all platforms</a>
</div>
