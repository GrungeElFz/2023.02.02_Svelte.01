<script>
  let count = 0;
  function increment() {
    count += 1;
  }
</script>

<button on:click={increment}>{count} Clicks</button>



<style>
  button {
    padding: 1rem 2rem;
    margin: 1rem auto 2rem;
  }
</style>