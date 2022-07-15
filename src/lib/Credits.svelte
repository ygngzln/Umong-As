<script lang="ts">
    let nameList:Array<string> = ["Egg - Website/Frontend", "Ygngzln - Website/Frontend", "UwUMan69303 - Data/Backend", "The Rock - Art/Maps/Game UI", "Truemong Trust - Game/Data", "Sussy Baka Productions - Game/Advertising", "Big Man - Somehow Everything", "[object] [Object] - Emotional Support"]
</script>

<fieldset id="cont">
    <legend> C R E D I T S </legend>
    {#each nameList as name}
        <div class="name">{name}</div>
    {/each}
</fieldset>

<footer>All of these are made up</footer>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Splash&display=swap');
    #cont {
        margin-top: 24px;
        padding: 24px;
        border: 40px groove darkgoldenrod;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
        background: url('../assets/he.jpeg');
        background-size: 925px;
    }

    legend {
        animation: title 60s infinite;
        font-weight: bold;
        border-radius: 18px;
        font-size: 40px;
        padding: 4px 8px;
        font-family: 'Splash', cursive;
    }

    footer {
        position: absolute;
        bottom: 0;
        left: 20%;
        font-size: 8px;
        transform: translateX(-50%);
        color: white;
    }
    @keyframes title {
        0% {
            color: cyan;
            background: linear-gradient(blue, deepskyblue);
        }
        15% {
            color: blue;
            background: linear-gradient(steelblue, steelblue);
        }
        30% {
            color: cyan;
            background: linear-gradient(blue, deepskyblue);
        }
        45% {
            color: blue;
            background: linear-gradient(steelblue, royalblue);
        }
        60% {
            color: blue;
            background: linear-gradient(steelblue, royalblue);
        }
        75% {
            color: cyan;
            background: linear-gradient(blue, steelblue);
        }
        90% {
            color: blue;
            background: linear-gradient(steelblue, deepskyblue);
        }
        100% {
            color: cyan;
            background: linear-gradient(blue, deepskyblue);
        }
    }

    .name {
        background: linear-gradient(dimgray, darkgray, silver);
        border-bottom: 28px solid gray;
        padding: 10px 14px;
        color: black;
        font-size: 18px;
        font-weight: bold;
        font-family: Monaco;
        text-align: center;
    }
</style>