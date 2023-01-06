<script>
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();
    
    function blowUpWorld() {
        // setTimeout(() => {
            dispatch('explosion', {
                text: '🔥BOOM! The world selfdestructed!🔥'
            });
        // }, 5000);
    }
</script>

<button class="btn" on:click={blowUpWorld}>Blow up World</button>