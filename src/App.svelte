<script>
  import HelloDesktop from "./HelloDesktop.svelte";
  import HelloMobile from "./HelloMobile.svelte";

  import MediaQuery from "./MediaQuery.svelte";
</script>

<main>
  <MediaQuery query="(min-width: 500px) and (max-width: 1280px)" let:matches>
    {#if matches}
      <HelloDesktop />
    {/if}
  </MediaQuery>

  <MediaQuery query="(max-width: 499px)" let:matches>
    {#if matches}
      <HelloMobile />
    {/if}
  </MediaQuery>
</main>

<style>
</style>
