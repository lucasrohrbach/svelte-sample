<script>
    export let result;
    function randomNumber(){
        result = Math.floor(Math.random()*1000);
    }
</script>
<button class="btn" on:click={randomNumber}>Execute random number of Civilians</button>