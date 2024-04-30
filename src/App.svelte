<script>
  let count = 0;
  function handleClick() {
    count += 1;
  }
  function handleClickEvent(event, stepSize) {
    count += stepSize;
  }
</script>

<main>
  <button on:click={() => (count = count + 1)}>Count {count}</button>
  <button on:click={handleClick}>Count {count}</button>
  <button on:click={(event) => handleClickEvent(event, 5)}>Count {count}</button
  >
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
