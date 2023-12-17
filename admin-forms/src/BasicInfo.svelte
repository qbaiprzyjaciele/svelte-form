<script>
    export let continueCallback;
    let name = '';
    let lastName = '';
    let phoneNumber = '';
</script>

<div>
    <label for="name">Name:</label>
    <input type="text" bind:value={name} id="name">

    <label for="lastName">Last name:</label>
    <input type="text" bind:value={lastName} id="lastName">

    <label for="phoneNumber">Phone number:</label>
    <input type="tel" bind:value={phoneNumber} id="phoneNumber">

    <button on:click={continueCallback}>Next</button>
</div>