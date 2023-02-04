<script>
  import Counter from "./lib/Counter.svelte";

  let name = 'Svelte'
  let logo = 'https://kit.svelte.dev/_app/immutable/assets/svelte-logo-5c5d7d20.svg'
  let text = 'This is a <strong>HTML</strong> string test.'
</script>

<img alt='logo' src={logo}>
<h1>Test: {name}</h1>
<p>{@html text}</p>

<Counter />



<style>
  img {
    width: 15rem;
  }
  h1 {
    color: orangered;
  }
</style>