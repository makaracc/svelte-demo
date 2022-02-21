<script>
  import Profile from "./Profile.svelte";
  import {auth, provider, signinGooPop} from './firebase.js';
  import {authState} from 'rxfire/auth';
import App from "./App.svelte";

  let user = authState(auth);
  // const unsubscript = authState(auth).subscribe(u => user = u);

  function login () {
    signinGooPop(auth, provider);
  }
</script>


<section>
  {#if $user}
    <Profile {...$user} />
    <button on:click={()=>{auth.signOut()}}>Logout</button>
    <hr>
    <Todo uid={$user.uid}/>
  {:else}
    <button on:click={login}>Login with google</button>
  {/if}
</section>