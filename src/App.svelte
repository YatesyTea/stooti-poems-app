<script>
  import Card from './lib/Card.svelte'
  const currentDate = new Date();
  const month = currentDate.getMonth() +1;
  const day = currentDate.getDate();
  const year = currentDate.getFullYear();
</script>

<main>
  <h1>Stooti's Random Poem of the Day</h1>
  <p>Today's Date is {day}-{month}-{year}</p>
  <div>
    <Card />
  </div>
</main>

<style>

</style>
