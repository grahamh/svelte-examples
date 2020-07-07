<script>
    let rev="";

function reverseString(str) {
    
    return str.split("").reverse().join(""); 
}

</script>

<style>

</style>


<!-- code to display the component goes here -->
<input bind:value={rev} placeholder="Text to reverse">

<div>
    {reverseString(rev)}
</div>

