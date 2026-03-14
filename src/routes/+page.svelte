<script lang="ts">
    import Rsvp from  "../lib/assets/Rsvp.svelte"
</script>

<style>
    :global(body) {
        margin: 0;
        padding: 0;
        background: white;
    }

    .land {
        width: 100%;
        margin: 0;
        padding: 0;
    }

    .landing {
        height: 100vh;
        position: relative;
        overflow: hidden;
    }

    .landing::before {
        content: '';
        background: url('/src/lib/images/step-team.webp');
        width: 100%;
        height: 100%;
        position: absolute;
        filter: brightness(60%);
        background-size: cover;
        top: 0;
        left: 0;
        z-index: -1;
        overflow: hidden;
    }

    .intro {
        display: flex;
        justify-content: column;
        flex-direction: column;
        align-items: center;
        position: relative;
        color: white;
        z-index: 1;
        font-family: 'Archivo Variable';
    }
    .ti {
        margin-top: 0;
        margin-bottom: 0;
        font-size: 1.5rem;
    }
</style>

<div class='land'>
<div class='landing'>

<div class='intro'>

<h1 style="color: yellow; font-size: 4rem; margin: mt-40;">Summer at home?</h1>  <!-- Will be a slider! --> 
<p class="ti" >join one of our free summer coding clubs near you,</p>
<p class="ti">or host your own, with friends!</p>

<Rsvp />

</div>

</div>
<h1>meow</h1>
</div>