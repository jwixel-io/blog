<script>
    import PostCard from './components/PostCard.svelte';

    export let name;
    let postcards = [ ];

    function handleAdd(e) {
        postcards = [...postcards, {title: "Bruno", content: "Uptown funk you up..."}];
    }
</script>

<style>
    h1 {
        color: purple;
    }
    #board {
        min-width: 800px;
        margin: 6px;
        background-color: #eee;
        min-height: 400px;
        padding: 1em;
    }
    .toolbar {
        width: 145px;
        min-height: 45px;
    }
    .button {
        width: 55px;
        padding: 8px;
        display: inline;
        float: left;
        font-size: x-large;
        cursor: pointer;
        text-align: center;
    }
    .button:hover {
        background-color: #99ccdd;
    }
</style>


<h1> Mosaic </h1>
<div class="toolbar">
    <div class="button" on:click={handleAdd}> + </div>
    <div class="button"> - </div>
</div>
<div id="board">
    {#each postcards as pc, i}
        <PostCard {...pc} />
    {/each}
</div>
