<script>
    let password;
    let password_again;
</script>

<style>

</style>


<!-- code to display the component goes here -->
<input placeholder="Name">
<input type="password" bind:value={password} placeholder="Enter Password">
<input type="password" bind:value={password_again} placeholder="Re-Enter Password">
{#if password==password_again}
    <div style="color:green">OK</div>
{:else}
    <div style="color:red">Passwords don't match</div>
{/if}
