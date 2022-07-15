<script lang="ts">
  import {Route, Router, Link} from 'svelte-routing';
  import Homepage from './lib/Homepage.svelte';
  import Shop from './lib/Shop.svelte'
  import News from './lib/News.svelte'
  import FAQ from './lib/FAQ.svelte'
  import Download from './lib/Download.svelte'
  import Credits from './lib/Credits.svelte'
  import Tutorial from './lib/Tutorial.svelte';
  import Media from './lib/Media.svelte'
  import PageLink from './lib/PageLink.svelte'
  import Major from './lib/Major.svelte'
  import Patch from './lib/Patch.svelte'

  let appbar:any;

  let newsList:Array<any> = [
        {
            "date": "1000000000000000000000000 BC",
            "type": true,
            "message": "BRO WHAT DA DAWG DOIN???? (Version 3 Release)",
            "notes": ["+ 1 Donator-Only Map", "+ 1 Donator-Only Character", "+ Released Umong As Merch And Plushie", "+ Accounts", "+ Reworked Database Once Again", "+ Ugraded Shop/Upgraded Website", "- \"XT-55Z\ Map (Replaced With 3X-TE11 Map)", "- \"Autopilot\" Sabatoge (Too OP)", "Fixed 8333333388121 Bugs"],
            "id": "233393"
        },
        {
            "date": "Universe Creation",
            "type": true,
            "message": "My name is Barry Allen and I'm the fastest man alive (Version 2 Release + Anticheat Update)",
            "notes": ["+ 2 New Maps", "+ Even More Characters", "+ \"Saturn Rings\" Map Redesign", "+ 2 Tasks", "+ Sus Sabotages", "+ Better Lighting", "+ New Role: The JESTER", "+ Blindcat Anticheat Added... No More Hackers :)", "- \"Update Star Map\" Task Removed", "- Character, \"Dream\", Removed (replaced with the better looking Jreem)", "Fixed 8331 Bugs"],
            "id": "330328"
        },
        {
            "date": "3000 Years BU",
            "type": true,
            "message": "It's MORBIN time!!! (Version 1 Release)",
            "notes": ["+ 4 New Maps", "+ New Characters", "+ New Lobbyfinder" + "+ Better UI", "+ More Tasks", "+ Changeable Character Colors", "+ Faster Netcode", "+ Reworked Database And Optimized", "Fixed 153 Bugs"],
            "id": "445223"
        },
        {
            "date": "3002 Years BU (Before Universe)",
            "type": true,
            "message": "Red Sus? (Version 0 Release)",
            "notes": ["+ Initial Release", "+ 4 Characters", "+ \"Big Uranus Base\" Map"],
            "id": "100000"
        }
    ]

  function titleenter(){
    appbar.style.background = 'radial-gradient(salmon, red, crimson, darkred)';
  }

  function titleout(){
    appbar.style.background = 'radial-gradient(cyan, aqua, skyblue, lightskyblue)';
  }
</script>

<Router url="">
<div id="appBar" bind:this={appbar}>
  <span id="left" class="pages">
    <Link to="/media"><PageLink linkName="Media" /></Link>
    <Link to="/news/"><PageLink linkName="News" /></Link>
    <Link to="/download"><PageLink linkName="Download Game" /></Link>
  </span>
  <Link to="/"><span id="title" on:mouseenter={titleenter} on:mouseleave={titleout}>Umong As</span></Link>
  <span id="right" class="pages">
    <Link to="/shop"><PageLink linkName="Shop" /></Link>
    <Link to="/faq"><PageLink linkName="FAQ" /></Link>
    <Link to="/credits"><PageLink linkName="Credits" /></Link>
    <Link to="/tutorial"><PageLink linkName="Tutorial" /></Link>
  </span>
</div>
<div id="pageBar">
  <Route path="shop"><Shop /></Route>
  <Route path="news"><News newsList={newsList}/></Route>
  {#each newsList as news}
      {#if news.type}
      <Route path='{news.id}'><Major major={news}/></Route>
      {:else}
      <Route path='{news.id}'><Patch patch={news}/></Route>
      {/if}
  {/each}
  <Route path="media"><Media /></Route>
  <Route path="download"><Download /></Route>
  <Route path="credits"><Credits /></Route>
  <Route path="faq"><FAQ /></Route>
  <Route path="tutorial"><Tutorial /></Route>
  <Route path="/"><Homepage /></Route>
</div>
</Router>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Edu+QLD+Beginner&display=swap');
  #appBar {
    width: 100%;
    height: 120px;
    line-height: 120px;
    background: radial-gradient(cyan, aqua, skyblue, lightskyblue);
    position: absolute;
    top: 0;
    right: 0;
    text-align: center;
  }

  #title {
    font-size: 75px;
    font-family: 'Edu QLD Beginner', cursive;
    display: inline-block;
    vertical-align: middle;
    line-height: normal;
    color: yellow;
    font-weight: bold;
  }

  #title:hover {
    color: orangered;
    border-radius: 20%;
    font-style: italic;
    cursor: pointer;
    background: url('./assets/he.jpeg');
  }

  .pages {
    display: inline-block;
    vertical-align: text-top;
    line-height: normal;
  }

  #pageBar {
    margin-top: 120px;
  }
</style>