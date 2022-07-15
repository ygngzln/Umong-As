<script lang="ts">
    import {fade} from 'svelte/transition'
    import {Router, Route, Link} from 'svelte-routing'
    export let newsList;
</script>

<div id="title" transition:fade="{{duration: 200}}"><div id="a">NEWS</div></div>

<Router url="">
<div id="cont" transition:fade="{{duration: 200}}">
{#each newsList as news}
    <div class="date">Date: {news.date}</div> <br />
    <Link to='/{news.id}'><button class="btn">{news.message}</button></Link><br/>
{/each}
</div>
</Router>

<style>
    :global(body)::-webkit-scrollbar {
        background: salmon;
        width: 4px;
    }

    :global(body)::-webkit-scrollbar-thumb {
        background: darkred;
    }

    #title {
        padding-top:15px;
        font-size: 80px;
        font-family: cursive;
        color: white;
        text-align: center;
    }

    #a {
        background-color:black;
        padding: 20px 90px 20px 90px;
        border-radius: 30%;
        display: inline-block;
        width: 35%;
    }

    #cont {
        margin-top: 20px;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        font-family: Monaco;
        background: black;
        width: 75%;
        text-align: center;
        padding: 20px 0 80px 0;
        background: url('../assets/red.png');
        background-size: 1050px;
        background-position-y: -250px;
        background-position-x: 65px;
        background-color: black;
        border-radius: 4em;
    }

    .date {
        margin-top: 20px;
        color: white;
        background-color: rgb(0,0,0,0.4);
        display: inline-block;
        padding: 5px 10px;
        border-radius: 1em 1em 0 0;
    }

    .btn {
        border: 4px solid white;
        background: url('../assets/amogusplace.jpeg');
        color: white;
        font-family: fantasy;
        font-size: 24px;
    }

    .btn:hover {
        font-size: 25px;
        border: 8px solid silver;
        color: violet;
        background: url('../assets/cosmos.jpeg');
        background-size: 1500px;
        font-weight: bold;
    }
</style>