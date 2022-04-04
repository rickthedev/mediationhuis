<script>
  import Header from "./lib/Header.svelte";
</script>

<main>
  <Header></Header>
</main>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
  }

  :global(ul) {
    list-style-type: none;
  }

  :global(a) {
    text-decoration: none;
    color: inherit;
  }

  :global(html) {
    font-family: "Swear Text";
  }

  :global(h1, h2, h3, h4, h5, h6) {
    font-family: "Swear Display";
    font-weight: bold;
  }
</style>