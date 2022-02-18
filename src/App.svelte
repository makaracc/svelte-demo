<script lang="ts">
  import logo from './assets/svelte.png'
  import Counter from './lib/Counter.svelte'

  let show = false;
  const setShow = () => show = !show;



</script>

<main>
  <button on:click={setShow}> </button>
 
</main>

<style>


 
</style>
