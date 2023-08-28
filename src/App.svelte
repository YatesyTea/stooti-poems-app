<script>
  import Card from "./lib/Card.svelte";
  const currentDate = new Date();
  const month = currentDate.getMonth() + 1;
  const day = currentDate.getDate();
  const year = currentDate.getFullYear();
</script>

<main>
  <img
    class="rounded-pic"
    src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.Noi4l9ejSc3y5vqicwihngHaJ4%26pid%3DApi&f=1&ipt=37f1410e6a90859d1d267f031e8b2216cb92a6e49fec81de147ec520c0f8e6cd&ipo=images"
    alt='stooti'
  />
  <h1>Stuti's Random Poem of the Day</h1>
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
