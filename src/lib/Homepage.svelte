<script lang="ts">
    import umogas from '../assets/umogas.png'
    let splash:any;

    let randomList:Array<any> = ["2020 Hit Game!", "Red Sus", "Imposter!!", "I have the high ground!", "Umogas", "Wut da dawg doin?", "Hacker!!!", "RED VENTED", "Which planet is this???", "Robux."]
    let x = Math.floor(Math.random()*randomList.length)
</script>

<div class="center">
    <div id="subtext">Official Site</div>
</div>
<div id="info">
    Umong As is a FREE TO PLAY game that is cross-platform (Windows, Mac, Linux, Mobile, AND even on the Ninetondo Gamerboy).
    This 2020 HIT GAME will blow your mind!!!!!1111!!!
</div>
<div id="pcount">
    69 Morbillion Total Players
</div>
<div id="leftc">

</div>
<div id="rightc">

</div>
<div id="splashtext" bind:this={splash}>{randomList[x]}</div>

<img src={umogas} alt="Umogas No Load" width="900" height="800"/>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Gentium+Book+Plus&display=swap');

    img {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        bottom: 0;
        top: 50px;
        z-index: -1;
        opacity: 0.72;
    }

    #leftc {
        position: absolute;
        left: 0%;
        width: 22.4%;
        height: 89%;
        background: url('../assets/red.png');
        background-size: 850px;
        transform: scaleX(-1);
        background-color: silver;
        background-position-x: 4px;
        border-radius: 40px 0 0 40px;
    }

    #rightc {
        position: absolute;
        left: 77.5%;
        width: 22.4%;
        height: 89%;
        background: url('../assets/white.png');
        background-size: 850px;
        background-color: red;
        background-position-x: 4px;
        border-radius: 40px 0 0 40px;
    }

    #pcount {
        color: white;
        font-size: 20px;
        left: 65%;
        font-style:italic;
        text-decoration: underline;
        position: absolute;
        transform: translateX(-50%);
        top: 690px;
    }

    #subtext {
        font-size: 40px;
        font-family: Monaco;
        background-color: crimson;
        color: white;
        margin-top: 135px;
        padding: 5px 15px;
    }

    #info {
        top: 500px;
        font-size: 25px;
        color: silver;
        background-color: black;
        font-family: Monaco;
        border-radius: 3em;
        padding: 1.5em;
        left: 50%;
        transform: translateX(-50%);
        position: absolute;
    }

    #splashtext {
        color: white;
        font-family: 'Gentium Book Plus', serif;
        transform: rotate(-37deg) translateX(-50%);
        position: absolute;
        background: rgb(0,0,0,0.3);
        border-radius: 2em;
        padding: 2px 4px;
        left: 66%;
        top: 180px;
        animation: splash 1.5s infinite;
    }

    @keyframes splash {
        0% {
            font-size: 25px;
        }
        5% {
            font-size: 27px;
        }
        10% {
            font-size: 29px;
        }
        15% {
            font-size: 31px;
        }
        20% {
            font-size: 33px;
        }
        25% {
            font-size: 35px;
        }
        30% {
            font-size: 37px;
        }
        35% {
            font-size: 39px;
        }
        40% {
            font-size: 41px;
        }
        45% {
            font-size: 43px;
        }
        50% {
            font-size: 45px;
        }
        55% {
            font-size: 43px;
        }
        60% {
            font-size: 41px;
        }
        65% {
            font-size: 39px;
        }
        70% {
            font-size: 37px;
        }
        75% {
            font-size: 35px;
        }
        80% {
            font-size: 33px;
        }
        85% {
            font-size: 31px;
        }
        90% {
            font-size: 29px;
        }
        95% {
            font-size: 27px;
        }
        100% {
            font-size: 25px;
        }
    }

    .center {
        margin-top: 15px;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
    }
</style>