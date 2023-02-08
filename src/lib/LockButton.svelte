<script>
  let lockStatus = false;
  function switchLock() {
    if (lockStatus) {
      lockStatus = false;
    } else if (!lockStatus) {
      lockStatus = true;
    }
  }
</script>


<button on:click={switchLock}>
  {#if lockStatus}
    Button is unlocked
  {:else if !lockStatus}
    Button is locked
  {/if}
</button>



<style>
  button {
    padding: 1rem 2rem;
    margin: 1rem auto 2rem;
  }
</style>