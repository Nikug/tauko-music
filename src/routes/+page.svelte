<script lang="ts">
  import { releases } from '$lib/releases';
  const orderedReleases = releases.sort((a, b) => b.date.getTime() - a.date.getTime());
</script>

<div class="px-8 py-12">
  <div class="w-min rounded bg-gray-300 px-4 pb-1">
    <h1 class="text-6xl font-extrabold text-gray-900 uppercase">Tauko</h1>
  </div>
  <p class="mb-4 font-semibold text-gray-400">Chill and melodic bass music</p>
  <p>Feel free to contact me if you want to</p>
  <p class="mb-8">Contact: <a href="mailto:taukomusic@gmail.com">taukomusic@gmail.com</a></p>

  <h2 class="mb-2 text-2xl font-bold">Releases</h2>
  <div class="flex flex-wrap gap-4">
    {#each orderedReleases as release}
      <div
        class="min-w-64 shrink rounded border bg-gray-800 px-4 py-2 shadow-blue-800/50 transition-shadow hover:shadow-lg"
      >
        <h3 class="text-xl font-bold">{release.name}</h3>
        <p class="text-gray-400">{release.date.toLocaleDateString()}</p>
        <a href={release.link} class="text-blue-500 underline">Listen on all platforms</a>
      </div>
    {/each}
  </div>
</div>
