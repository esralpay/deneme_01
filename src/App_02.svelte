<script>
    import Buttonesra from "./Button.svelte";
    const log = () => {
        console.log("Button clicked");
    }

</script>
<main>
    <Buttonesra on:click={log}/>
    <button on:click={log}>App Button</button>
</main>
<style>
    main {
        display:flex;
        flex-direction: column;
        align-items: center;

    }
</style>