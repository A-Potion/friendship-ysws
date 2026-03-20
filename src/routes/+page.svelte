<script lang="ts">
    import sun from '$lib/images/sun.png';
    import orpheus from '$lib/images/flag-orpheus-top.png'
    import Rsvp from  "../lib/assets/Rsvp.svelte"
</script>

<style>

.orpheus {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 10;
}

.content {
    display: flex;
    flex-direction: row;
}

.land {
    position: relative;
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
     margin: 0;
    height: 100%;
    background-color: #52CFEB;
}

.summer {
    flex: 1;
}
.sun {
    flex: 1;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
}
img.sun {
    width: 30%;
    height: auto;
    
}
    
</style>

<div class='land'>
<div class='orpheus'>
    <img alt="Hack Club logo" src={orpheus} />
</div>
<div class='content'>
<div class='summer'>
<p>
    Hello, world!
</p>
</div>
<div class='sun'>
<img alt="Sun." src={sun} class='sun' />
</div>
</div>
</div>