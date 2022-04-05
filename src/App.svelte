<script>
  import Contact from "./lib/Contact.svelte";
  import Footer from "./lib/Footer.svelte";
  import Header from "./lib/Header.svelte";
  import Locatie from "./lib/Locatie.svelte";
  import Mediation from "./lib/Mediation.svelte";
  import Vertrouwenspersoon from "./lib/Vertrouwenspersoon.svelte";
</script>

<main>
  <Header />
  <Mediation />
  <Vertrouwenspersoon />
  <Locatie />
  <Contact />
  <Footer />
</main>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(html) {
    font-family: "Swear Text";
  }

  :global(h1, h2, h3, h4, h5, h6) {
    font-family: "Swear Display";
    font-weight: bold;
  }

  :global(ul) {
    list-style-type: none;
  }

  :global(a) {
    text-decoration: none;
    color: inherit;
  }

  :global(h2) {
    font-size: 3rem;
    margin-bottom: 1rem;
  }

  :global(h3) {
    font-size: 2rem;
    margin-bottom: 0.5rem;
  }

  main {
    overflow-x: hidden;
  }
</style>
