<script>
  import Card from "./lib/Card.svelte";
  import Stuti from "./assets/spachisia.jpg"
  const currentDate = new Date();
  const month = currentDate.getMonth() + 1;
  const day = currentDate.getDate();
  const year = currentDate.getFullYear();
</script>

<main>
  <img
    class="rounded-pic"
    src="{Stuti}"
    alt='stooti'
  />
  <h1>Stooti's Random Poem of the Day</h1>
  <p>Today's Date is {day}-{month}-{year}</p>
  <div>
    <Card />
  </div>
</main>

<style>
  .rounded-pic {
    border-radius: 9999px;
    max-height: 25vh;
  }
</style>
