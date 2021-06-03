<script>
    export let btnText="Component Button";

</script>
<div class="card" on:click>    
    <button>{btnText}</button>

</div>

<style>
    button {
        background : blue;
        border : red;
        color : white;
        }
    .card {
        padding: 20px;
        border: 10px solid black;
        margin-bottom: 8px;
    }
        

</style>