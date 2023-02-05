<script>
  export let size = 'small';
  export let shadow = false;

</script>



<button 
  class:size-sm={size === 'small'}
  class:size-lg={size === 'large'}
  class:shadow={shadow}>
  <slot>Fallback</slot>
</button>



<style lang="scss">
  button {
    border: none;
    background-color: variables.$color;
    color: white;
    font-weight: bold;
    border-radius: 5rem;
    cursor: pointer;
    &:hover {
      background-image: linear-gradient(orangered, red, orangered);
    }
    &:active {
      background-image: radial-gradient(circle, rgba(255,120,0,1) 0%, rgba(255,69,0,1) 50%, rgba(255,69,0,1) 100%);
    }
    &.size-sm {
      padding: 1rem 5rem;
      font-size: small;
    }
    &.size-lg {
      padding: 2rem 8rem;
      font-size: large; 
    }
    &.shadow {
      box-shadow: 0 0 5rem rgba(145, 200, 240, 0.6);
    }
  }
</style>