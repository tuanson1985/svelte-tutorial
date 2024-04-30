<script>
  let firstName = "Bui";
  let lastName = "Tuan Son";
  $: fullName = `${firstName} ${lastName}`;
  $: {
    const greet = `Fullname is ${firstName} ${lastName}`;
    console.log(greet);
  }
  let items = [
    {
      id: 1,
      title: "TV",
      price: 100,
    },
    {
      id: 2,
      title: "Phone",
      price: 200,
    },
    {
      id: 3,
      title: "Laptop",
      price: 300,
    },
  ];
  $: total = items.reduce((total, curr) => (total = total + curr.price), 0);

  $: console.log(`Fullname is ${firstName} ${lastName}`);
  let volume = 0;
  $: if (volume < 0) {
    alert(`Can't go lower`);
    volume = 0;
  } else if (volume > 20) {
    alert(`Can't go higher`);
    volume = 20;
  }
</script>

<main>
  <h2>{firstName} {lastName}</h2>

  <h2>{fullName}</h2>

  <button
    on:click={() => {
      firstName = "Son";
      lastName = "Bui Tuan";
    }}>Change Name</button
  >

  <h2>Reactive Total - {total}</h2>

  <button
    on:click={() =>
      (items = [...items, { id: 4, title: "Keyboard", price: 50 }])}
  >
    Add item
  </button>

  <div>
    <h2>Current Volume {volume}</h2>
    <button on:click={() => (volume += 2)}>Increase Volume</button>
    <button on:click={() => (volume -= 2)}>Decrease Volume</button>
  </div>
</main>

<style>
  input + label {
    display: inline-block;
  }
  main {
    /* text-align: center; */
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
