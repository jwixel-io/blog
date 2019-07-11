<script>
    export let title = 'Hello Austin';
    export let content = 'Sample content';

    function handleChange(e) {
    }
</script>

<style>
    .card {
        position: relative;
        float: left;
        width: 250px;
        height: 175px;
        background-color: #fffdd0;
        border: 2px solid black;
        border-radius: 6px;
        padding: 1em;
    }

    .title {
        font-size: larger;
        background-color: #ccc;
    }

    .content {
        font-size: smaller;
    }
</style>

<div class="card">
    <div class="title" contenteditable on:keyup={handleChange}>
        {title}
    </div>

    <div class="content" contenteditable on:keyup={handleChange}>
        {content}
    </div>
</div>
