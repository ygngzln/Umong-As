<script lang="ts">
    let a:any;
    function enter(){
        a.style.background = "repeating-linear-gradient(darkblue, blue)"
        a.style.color = "orangered"
        a.style.border = "14px solid darkred"
    }
    let src = window.location.href.replace("/download", "") + "/sussy.zip"
    
    function exit(){
        a.style.background = "repeating-linear-gradient(deepskyblue, lightblue)"
        a.style.color = "black"
        a.style.border = "12px double crimson"
    }
</script>

<a href={src} download="Umong-As-Game" bind:this={a} on:mouseenter={enter} on:mouseleave={exit}>Download</a>
<div>OR YOU SUSSY >:(</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Lobster+Two&display=swap');
    a {
        color: black;
        background: repeating-linear-gradient(deepskyblue, lightblue);
        font-size: 120px;
        left: 50%;
        transform: translateX(-50%);
        position: absolute;
        margin-top: 50px;
        text-decoration: none;
        padding: 40px;
        border-radius: 25%;
        font-family: 'Press Start 2p', cursive;
        font-style: italic;
        border: 12px double crimson;
    }
    div {
        color: white;
        font-size: 90px;
        position: absolute;
        left: 50%;
        font-weight: bold;
        transform: translateX(-50%);
        margin-top: 300px;
        width: 100%;
        text-align: center;
        font-family: 'Lobster Two', cursive;
    }
</style>