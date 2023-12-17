<script>
    export let continueCallback;
    export let backCallback;
    
    let email = '';
    let street = '';
    let streetNumber = '';
    let city = '';

</script>

<div>
    <label for="email">e-mail:</label>
    <input type="email" bind:value={email} id="email">
    
    <label for="street">Street:</label>
    <input type="text" bind:value={street} id="street">

    <label for="streetNumber">Building number</label>
    <input type="number" bind:value={streetNumber} id="streetNumber">

    <label for="city">City</label>
    <input type="text" bind:value={city} id="city">

    <button on:click={backCallback}>Back</button>
    <button on:click={continueCallback}>Next</button>
</div>