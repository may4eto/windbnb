<script>
  import data from "../stays.json"
  import Card from "./lib/Card.svelte";
import Footer from "./lib/Footer.svelte";
  import Header from "./lib/Header.svelte";
</script>

<Header />
<main>
  <h1>Stays in Finland</h1>
  <div class="grid">
    {#each data as item}
      <Card {item}></Card>
    {/each}
  </div>
</main>
<Footer />

<style>
  main {
    padding: 5rem 0;
    max-width: 80vw;
    margin: 0 auto;
  }
  h1 {
    font-size: 1.5rem;
    font-weight: 700;
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
</style>
