<script lang="ts">
    import sun from '$lib/images/sun.png';
    import hc_logo from '$lib/images/flag-orpheus-top.png'
    import Rsvp from  "$lib/assets/Rsvp.svelte"
    import How from "$lib/assets/How.svelte"
    import Faq from "$lib/assets/Faq.svelte"

    import { onMount } from 'svelte';

onMount(() => {
    history.scrollRestoration = 'manual';
    window.scrollTo(0, 0);
});
</script>

<style>

.top h1 {
    font-family: 'Hammersmith One', sans-serif;
    font-size: 12vh;
    font-weight: 100;
    margin-bottom: 0;
}

p {
    margin-top: 0;
    margin-left: 0.4vw;
    font-family: 'Hammersmith One', sans-serif;
    font-weight: 100;
    font-size: 3.85vh;
}

.main {
    background-color: #52CFEB;
}

.arrow {
  border: solid purple;
  border-width: 0 1vw 1vw 0;
  display: inline-block;
  padding: 3.5vh;
}

.down {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}

.goscroll {
    margin-top: auto;
    display: flex;
    align-items: center;
    justify-content: center;
}

.orpheus {
    position: absolute;
    top: 0;
    left: 0;
    padding-left: 1vw;
    z-index: 10;
}

.orpheus_logo {
    width: 40%;
    height: auto;
}

.uppercont {
    display: flex;
    flex-direction: column;
    padding-top: 4vh;
    padding-left: 1vw;
}

.top {
    display: flex;
    flex-direction: row;
    padding-top: 14vh;
    padding-left: 2vw;
}

.land {
    position: relative;
    width: 100%;
    min-height: 100vh;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
}

.summer {
    flex: 1;
    display: flex;
    flex-direction: column;
}
.yello {
    color: yellow;
}
.sun {
    position: absolute;
    top: 4vh;
    right: 2vw;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    overflow: hidden;
}

.sun_img {
    width: 35vw ;
    height: auto;
    animation: spin 1s ease-in-out forwards;
}
@keyframes spin { 
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}
    

.rsvp {
    width: 50vw;
    display: flex;
    align-items: center;
    justify-content: center;
   
}

.map {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2vh 0;
    background-color: #f5f5f5;
}

.map iframe {
    width: 70vw;
    height: 40vh;
    border: none;
    border-radius: 1vh;
    margin-bottom: 4vh;
}

.map h2 {
    margin-top: 2vh;
    font-family: 'Hammersmith One', sans-serif;
    font-size: 6vh;
    font-weight: 100;
    margin-bottom: 1vh;
}
    
</style>

<div class='main'>
<div class='land'>
<div class='orpheus'>
<a href='https://hackclub.com'>
    <img alt="Hack Club logo" src={hc_logo} class='orpheus_logo' />
</a>
</div>
<div class='uppercont'>
<div class='top'>
<div class='summer'>
<h1>
    Summer at <span class='yello'>home</span>?
</h1>
<div class='below'>
    <p>Join Sunshine, free, student-led coding clubs near you.</p>
</div>
<div class='rsvp'>
<Rsvp />
</div>
</div>
<div class='sun'>
<img alt="Sun." src={sun} class='sun_img' />
</div>
</div>
</div>
<div class="goscroll">
<p><i class="arrow down"></i></p>
</div>

</div>
<div class='map'>
    <h2>Find a Sunshine close to you</h2>
    <iframe src="/map" title="Map"></iframe>
</div>
<div id="how_section">
<How />
</div>

<div id="faq_section">
    <Faq />
</div>

</div>