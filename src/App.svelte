<script lang="ts">
  export let name;
  import Login from './Login.svelte';

</script>

<svelte:head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css">
</svelte:head>

<main>
  <h1>Hello {name}</h1>
</main>
