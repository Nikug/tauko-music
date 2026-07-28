<script lang="ts">
  import './layout.css';
  import favicon from '$lib/assets/favicon.svg';

  let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
  <meta
    name="description"
    content="Tauko is a producer and composer of chill and melodic bass music"
  />
  <title>Tauko</title>
</svelte:head>
{@render children()}
