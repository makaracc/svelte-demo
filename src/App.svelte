<script lang="ts">
  import logo from './assets/svelte.png'
  import Counter from './lib/Counter.svelte'

  let show = false;
  const setShow = () => show = !show;
</script>

<main>
  <button on:click={setShow}> </button>
  <button on:click={setShow}> </button>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

 
</style>
