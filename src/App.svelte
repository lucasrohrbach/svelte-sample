<script lang="ts">
    import Counter from "./lib/Counter.svelte";
    import Title from "./lib/Title.svelte";
    import Progress from "./lib/Progress.svelte";
    import Difference from "./lib/Difference.svelte";
    import Executor from "./lib/Executor.svelte";
    import Info from "./lib/Information.svelte";
    import Countdown from "./lib/Countdown.svelte";

    let progress: number = 0;
    let diffValue1 = 0;
    let diffValue2 = 0;
    $: diff = diffValue1 - diffValue2;

    $: textDiff = "Land available: " + diff + "%"
    let execute = 0;

    function handleMessage(event) {
        alert(event.detail.text);
    }
</script>

<main class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
        <div class="max-w-md gap-4">
            <Title/>
            <br>
            <br>
            <p>Land conquered:</p>
            <Difference bind:val={diffValue1}/>
            <p>Land burned:</p>
            <Difference bind:val={diffValue2}/>
            <div class="badge-error">{textDiff}</div>
            <br>
            <br>
            <Executor bind:result={execute}/>
            <p>{execute} Civilians Executed</p>
            <br>
            <br>
            <Counter bind:count={progress}/>
            <br>
            <br>
            <Progress  answer={progress}/>
            <br>
            <br>
            <Countdown on:explosion={handleMessage}/>
            <br>
            <br>
            <Info>
            </Info>
            
        </div>
    </div>
</main>
