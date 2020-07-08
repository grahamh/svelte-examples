<script>
    let cards=["🂡", "🂢", "🂣", "🂤", "🂥", "🂦", "🂧", "🂨", "🂩", "🂪", "🂫", "🂭", "🂮"];


let randomCard= "🂡";


    function getRandomCard() {
        var cardIndex = Math.floor(Math.random()*13);
        console.log(cardIndex);
        randomCard = cards[cardIndex];
    }


</script>

<style>

</style>


<!-- code to display the component goes here -->
<button on:click={getRandomCard}>Draw</button>
<div style="font-size:12em">{randomCard}</div>
