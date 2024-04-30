<script>
  import { shuffle } from "lodash";
  let names = [
    "Bui Tuan Son",
    "Do The Phuong",
    "Dang Van Truong",
    "Nguyen Tuan",
  ];
  const shuffleNames = () => {
    names = shuffle(names);
  };
</script>

<main>
  {#each names as name (name)}
    <h2>{name}</h2>
    <input placeholder="Last name" />
  {/each}
  <div>
    <button on:click={shuffleNames}>shuffle!</button>
  </div>
</main>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>
