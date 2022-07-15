<script lang="ts">
    import {Link} from 'svelte-routing'
    export let patch:any;
</script>

<div class="cont">
    Date: <div class="date">{patch.date}</div>
    <div class="message">{patch.message}</div>
    {#each patch.notes as note}
        <div class="notes">{note}</div>
    {/each}
</div>

<Link to="/news"><button id="back">Back</button></Link>

<style>
    #back {
        background-color: orange;
        border: 4px solid crimson;
        color: crimson;
        font-size: 24px;
        font-family: serif;
        z-index: 99;
        font-weight: bold;
        border-radius: 8px;
        margin-top: 50px;
        position: relative;
        margin-left: 50px;
    }

    #back:hover {
        font-size: 25px;
        background: url('../assets/amogusplace.jpeg');
        color: white;
        border: none;
        padding: 10px;
        cursor: pointer;
        border: 2px solid white;
    }

    .cont {
        margin-top: 20px;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        font-family: Monaco;
        background: black;
        text-align: center;
        color: white;
        padding: 20px 0 80px 0;
        width: 100%;
        border-radius: 2em;
        z-index: 1;
    }

    .date {
        margin-bottom: 25px;
        font-size: 12px;
    }

    .message {
        margin-bottom: 15px;
        font-weight: bold;
        font-size: 20px;
    }

    .notes {
        color: black;
        background-color: white;
        padding: 20px 0;
    }
</style>