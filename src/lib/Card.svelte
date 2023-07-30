<script>
  import jsonData from "../assets/PoetryFoundationData.json";
  
  const currentDate = new Date();
  const day = currentDate.getDate();
  const month = currentDate.getMonth() + 1; // Months are zero-based, so add 1
  const year = currentDate.getFullYear();

  const seed = day + month + year;
  const range = 13845;
  const randomValue = (seed % range) + 1;

  const selectedData = jsonData.find((item => item.id === randomValue));
  const tagsArr = selectedData.Tags ? selectedData.Tags.split(",") : [];
  console.log(selectedData);
</script>

<main>
  <div class="display">
    <h2>Poem #{selectedData.id} - {selectedData.Title}</h2>
    <h3>by {selectedData.Poet}</h3>
    <p class="line-break-text">{selectedData.Poem}</p>
    <div class="listbox-display">
      {#if tagsArr.length > 0}
        <p>Tags: {tagsArr}</p>
      {/if}
    </div>
  </div>
</main>

<style>
  .display {
    border-radius: 25px;
    background-color: #eee8d5;
    min-height: 50vh;
    padding: 2rem;
  }
  .line-break-text {
    white-space: pre-wrap;
  }
</style>
