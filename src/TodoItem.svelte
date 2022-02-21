<script>
  import {fly, fade} from 'svelte/transition';
  import {createEventDispatcher} from 'svelte';
  const dispatch = createEventDispatcher();

  function remove () {
   dispatch('remove', {id});
  }

  function toggleStatus () {
    let status = !complete;
   dispatch('toggle', {id, newStatus});
  }

  export let id;
  export let complete;
  export let text;
  export let newStatus;
</script>

<li>
  <p>{text}</p>
  {#if complete}
    <button on:click={toggleStatus}>
      y
    </button>
  {:else}
    <button on:click={toggleStatus}>
      x
    </button>
  {/if}
</li>