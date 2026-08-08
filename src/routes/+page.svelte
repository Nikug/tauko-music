<script lang="ts">
  import EmailButton from '$lib/components/EmailButton.svelte';
  import ProjectCard from '$lib/components/ProjectCard.svelte';
  import ReleaseCard from '$lib/components/ReleaseCard.svelte';
  import { releases } from '$lib/releases';
  const orderedReleases = releases.sort((a, b) => b.date.getTime() - a.date.getTime());
</script>

<div class="px-8 py-12">
  <div class="w-min rounded bg-gray-300 px-4 pb-1">
    <h1 class="text-6xl font-extrabold text-gray-900 uppercase">Tauko</h1>
  </div>
  <p class="mb-4 font-semibold text-gray-400">Chill and melodic bass music</p>
  <p>Feel free to contact me if you want to</p>

  <div class="mb-8 flex gap-2">
    <p>Contact:</p>
    <EmailButton />
  </div>

  <h2 class="mb-2 text-2xl font-bold">Releases</h2>
  <div class="mb-8 flex flex-wrap gap-4">
    {#each orderedReleases as release (release.link)}
      <ReleaseCard {release} />
    {/each}
  </div>

  <h2 class="mb-2 text-2xl font-bold">Other projects</h2>
  <div class="flex flex-wrap gap-4">
    <ProjectCard
      title="Solid Synth"
      description="A subtractive synthesizer right in your browser. Has three oscillators and multiple effects."
      link="https://nikug.github.io/solid-synth/"
    />
  </div>
</div>
