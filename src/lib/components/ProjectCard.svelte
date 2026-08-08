<script lang="ts">
  interface Props {
    title: string;
    description: string;
    link: string;
  }
  const { title, description, link }: Props = $props();
</script>

<div
  class="max-w-sm min-w-64 shrink rounded border bg-gray-800 px-4 py-2 shadow-blue-800/50 transition-shadow hover:shadow-lg"
>
  <h3 class="text-xl font-bold">{title}</h3>
  <p class="text-gray-400">{description}</p>
  <a href={link} rel="external" class="text-blue-500 underline">Visit project</a>
</div>
