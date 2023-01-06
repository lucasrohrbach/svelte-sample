<script lang="ts">
    export let count: number = 0;
    const increment = () => {
        count += 1;
    };
    const decrement = () => {
        count -= 1;
    };
</script>

<div class="btn-group">
    <button class="btn">Humans Killed: {count}0 Mill</button>
    <button class="btn" on:click={increment}>+</button>
    <button class="btn" on:click={decrement}>-</button>
</div>