<script>
  export let name;
  export let profile;
  export let uid;
</script>

<main>
  <h3>Hi {name}</h3>
  <img src={profile} alt={`${name} profile`} width="100">
  <h3>Your UID {uid}</h3>
</main>