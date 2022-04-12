<script>
import '@lottiefiles/lottie-player'
import {
    fly,
    fade
} from 'svelte/transition';
let loading = true
let faded = null

setTimeout(() => {
    loading = false
    handleFade()
}, 2000);

function handleFade(params) {
    setTimeout(() => {
        faded = true
    }, 500);
}
</script>

{#if loading}
<div style="width: 100%; height:60vh; display:flex; justify-content:center; align-items:center" out:fade>
    <lottie-player
        autoplay
        loop
        mode="normal"
        id="firstLottie"
        src="https://assets7.lottiefiles.com/packages/lf20_ZCjq5s.json"
        style="width:200px; height: 200px;"
        >
    </lottie-player>
</div>
{:else if faded}
<div in:fade  style="width: 100%; display:flex; justify-content:center">
    
    <video style="width:90%" src="https://res.cloudinary.com/do4mactw0/video/upload/v1649796707/HeroComponent.svg_-_Animation_1_1_xiciwd.mp4" autoplay muted loop/>
        </div>
        <div style="position: absolute;display:flex; flex-direction: column; align-items:center; left: 50%; transform: translate(-50%, 0); bottom:10px">
            <span style="font-size: x-small;">SCROLL</span>
            <video style="height: 1.6rem;" src="https://res.cloudinary.com/do4mactw0/video/upload/v1649798889/New_Artboard_-_Animation_1_kjncyn.mp4" autoplay muted loop></video>
        </div>
        <div in:fade style="width:87vw; position:relative">
            <img style="position: absolute; bottom:0px; right:10px;" src="https://res.cloudinary.com/do4mactw0/image/upload/v1649799532/Group_1_uxd6of.png" alt="icons">
        </div>

        {/if}

<style>

</style>
