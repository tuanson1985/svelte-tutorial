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
