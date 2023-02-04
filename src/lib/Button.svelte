<script>

</script>



<button><slot>Fallback</slot></button>



<style lang="scss">
  button {
    border: none;
    background-color: orangered;
    color: white;
    padding: 1rem 5rem;
    font-weight: bold;
    border-radius: 5rem;
    cursor: pointer;

    &:hover {
      background-color: rgb(255, 100, 50);
    }
  }
</style>