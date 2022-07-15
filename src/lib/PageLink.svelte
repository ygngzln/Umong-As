<script lang="ts">
    export let linkName:string;
</script>

<span class="pageL">{linkName}</span>

<style>
    .pageL {
        display: inline-block;
        position: sticky;
        vertical-align: middle;
        font-size: 25px;
        font-family: fantasy;
        font-weight: bold;
        margin: 0 25px;
        color: black;
        padding: 4.5px;
    }

    .pageL:hover {
        background: url('../assets/amogusplace.jpeg');
        border-radius: 10px;
        cursor: pointer;
        color: white;
    }
</style>