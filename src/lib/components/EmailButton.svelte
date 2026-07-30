<script lang="ts">
  let visible = $state(false);
</script>

{#if visible}
  <a href="mailto:taukomusic@gmail.com">taukomusic@gmail.com</a>
{:else}
  <button
    class="cursor-pointer font-bold text-blue-500 hover:text-blue-600"
    onclick={() => (visible = true)}
  >
    Show email
  </button>
{/if}
