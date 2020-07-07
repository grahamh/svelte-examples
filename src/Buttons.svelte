<script>
    let count = 0;

function increment() {
    count += 1;
}

function decrement() {
    count -=  1;
}

</script>

<style>

</style>


<!-- code to display the component goes here -->
<div>
    <button on:click={increment}>+</button>
    <div>{count}</div>
        <button on:click={decrement}>-</button>
</div>    
