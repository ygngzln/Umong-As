<script lang="ts">
    import red from '../assets/shopitems/umogasplushiered.png'
    import blue from '../assets/shopitems/umogasplushieblue.png'
    import pink from '../assets/shopitems/umogasplushiepink.png'
    import hat from '../assets/shopitems/umonghat.png'
    import sun from '../assets/shopitems/sun.png'
</script>

<div id="cont">
    <div class="plush">
        <img id="red" src={red} alt="Plush no load :(" />
        <span class="text"> RED PLUSHIE 6in x 12in x 2in <span class="cost">$69.99</span> </span>
    </div>
    <div class="plush">
        <img id="blue" src={blue} alt="Plush no load :(" />
        <span class="text">BLUE PLUSHIE 6in x 12in x 2in <span class="cost">$69.99</span></span>
    </div>
    <div class="plush">
        <img id="pink" src={pink} alt="Plush no load :(" />
        <span class="text">PINK PLUSHIE 6in x 12in x 2in <span class="cost">$69.99</span></span>
    </div>
    <div id="hat">
        <img id="hat" src={hat} alt="Hat no load :(" width="200" height="200"/>
        <span class="text">GRAY UMOGAS HAT <span class="cost">$420.69</span></span>
    </div>
    <div id="sun">
        <img id="sun" src={sun} alt="Sun no load :(" width="200" height="200"/>
        <span class="text">1x1 MODEL OF THE "SUN" MAP Diameter: 865,000 Miles <span class="cost">$Your Soul</span></span>
    </div>
</div>

<footer>-none of these are actually marketed or owned by me-</footer>

<style>
    #cont {
        background: rgb(0,0,0, 0.5);
        position: absolute;
        top: 170;
        left: 0;
        width: 100%;
    }

    footer {
        position: absolute;
        left: 50%;
        bottom: -115%;
        transform: translateX(-50%);
        font-size: 9px;
        color: white;
    }

    div {
        color: white;
        position: relative;
    }

    .text {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        font-size: 40px;
        font-family: Monaco;
        font-weight: bold;
    }
    
</style>