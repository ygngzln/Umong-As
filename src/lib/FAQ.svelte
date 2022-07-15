<script lang="ts">
    let questionList:Array<any> = [
        {
            q: "Why are you like this?",
            a: "UMOGAS"
        },
        {
            q: "Are you high again?",
            a: "UMOGAS"
        },
        {
            q: "How download??? It not open?",
            a: "UMOGAS"
        },
        {
            q: "Is this game open source?",
            a: "UMOGAS"
        },
        {
            q: "Is it on the Switch/Xbox/Playstation/Calculator?",
            a: "UMOGAS"
        },
        {
            q: "How to is yes go where there?",
            a: "UMOGAS"
        }
    ]
</script>

<div id="cont">
{#each questionList as q}
    <div class="q">Question: {q.q}</div>
    <div class="a">My answer: <br /><strong>{q.a}</strong></div>
{/each}
</div>

<style>
    #cont {
        margin-top: 20px;
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        font-family: Monaco;
        background: white;
        width: 75%;
        text-align: center;
        padding: 20px 0 80px 0;
        color: white;
        border-radius: 18px;
    }

    .q {
        font-size: 34px;
        margin-top: 30px;
        font-family: Monaco;
        text-decoration: underline;
        background: black;
        padding: 10px 0;
    }

    .a {
        font-size: 28px;
        padding: 5px 0 10px 0;
        font-family: cursive;
        background: black;
    }
</style>