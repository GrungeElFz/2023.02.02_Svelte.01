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


<button on:click={switchLock}
  class:button-unlocked={lockStatus}
  class:button-locked={!lockStatus}
>
  {#if lockStatus}
    Button is unlocked
  {:else if !lockStatus}
    Button is locked
  {/if}
</button>



<style>
  button {
    display: flex;
    align-items: center;
    margin-bottom: 2rem;
    color: var(--buttonTextColor);
    border: none;
    border-radius: 5rem;
    font-weight: bold;
    cursor: pointer;
  }
  .button-unlocked {
    background-color: rgb(80, 200, 80);
    padding: 0.5rem 6rem;
  }
  .button-locked {
    background-color: red;
    padding: 0.5rem 6.5rem;
  }
</style>