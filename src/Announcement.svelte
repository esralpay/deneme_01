<script>
    let show = true;
    const hideAlert =() => {
        show = false;
    }
    let warning = true;

</script>
{#if show}
    <div class= "alert" class:warning={warning}>
        50 off all fruits. Buy it now.
        <button on:click={hideAlert}>Hide</button>
    </div>
{/if}
<style>
    .alert{
        padding: 8px;
        font-size: 18px;
        background-color: green;
        color: white;
    }
    .warning{
        padding: 8px;
        font-size: 18px;
        background-color: red;
        color: white;
    }

</style>