
<script>
    export let answer;
</script>

<p>Overall world domination:</p>
<progress class="progress w-56" value="{answer}" max="100"></progress>
<br>
{#if answer < 50}
    <div class="badge-error">Bad - Kill More Humans!</div>
{:else if answer >= 100}
    <div class="badge-success">Good - You are dominating the world!</div> 
{:else} 
    <div class="badge-warning">Better - We are getting there!</div>
{/if}


