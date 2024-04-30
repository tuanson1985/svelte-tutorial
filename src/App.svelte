<script>
  const name = "HQGROUP";
  const channel = "<b>Condevolution</b>";
  const hack = `<a href="#" onclick="alert('You have been hacked!')">Win pzize!</a>`;
  const id = "heading";
  const disabled = true;
  const status = "success";
  const isPromoted = true;
  const promoted = true;
</script>

<main>
  <h2 class="underline">Underlined Text</h2>
  <h2 class={status}>Status</h2>
  <h2 class={isPromoted ? "promoted" : ""}>Movie Title</h2>
  <h2 class:promoted={isPromoted}>Movie Title</h2>
  <h2 class:promoted>Movie Title</h2>

  <h1>Hello {name}!</h1>
  <div>{@html channel}</div>
  <div>{@html hack}</div>
  <h2 {id}>This is a heading</h2>
  <button {disabled}>Bind</button>
</main>

<style>
  .underline {
    text-decoration: underline;
  }

  .danger {
    color: red;
  }

  .success {
    color: olivedrab;
  }

  .promoted {
    font-style: italic;
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
