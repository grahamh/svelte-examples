<script>
    let no=1;

function handleClick() {
    no = Math.floor(Math.random()*6)+1;
}

</script>

<style>

</style>


<!-- code to display the component goes here -->
<div>{no}</div>
<button on:click={handleClick}>Roll</button>

