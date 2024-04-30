<script>
  const formValues = {
    name: "",
    profileSummary: "",
    country: "",
    jobLocation: [],
  };
</script>

<main>
  <div>
    <pre>
		{JSON.stringify(formValues, null, 2)}
	</pre>
  </div>
  <form>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" bind:value={formValues.name} />
    </div>

    <div>
      <label for="profile">Profile Summary</label>
      <textarea name="" id="profile" bind:value={formValues.profileSummary} />
    </div>

    <div>
      <label for="country">Country</label>
      <select id="country" bind:value={formValues.country}>
        <option value="">Select a country</option>
        <option value="india">India</option>
        <option value="vietname">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>

    <div>
      <label for="job-location">Job location</label>
      <select id="job-location" bind:value={formValues.jobLocation} multiple>
        <option value="">Select a country</option>
        <option value="php">PHP</option>
        <option value="java">Java</option>
        <option value="typescript">TypeScript</option>
      </select>
    </div>

	
  </form>
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
