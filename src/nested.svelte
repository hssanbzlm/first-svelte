<script>
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher();

    function random() {
        setTimeout(() => {
            let x = Math.random();
            dispatch("message", { text: x });
        }, 2000);
    }
</script>

<style>
    h1 {
        color: red;
    }
</style>

<button on:click={random}> Get random number </button>
