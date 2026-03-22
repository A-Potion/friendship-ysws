<script lang="ts">
    import deven from "$lib/images/talk.webp";
    import codetogether from "$lib/images/code.webp";
    import prizes from "$lib/images/prizes.webp";
</script>

<style>

#how {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    margin-bottom: 4vh;
}

#how h1 {
    font-family: 'Hammersmith One', sans-serif;
    font-size: 4.8vw;
    font-weight: 100;
    margin-bottom: 2vh;
}

#hows {
    display: flex;
    flex: 1;
    width: 80vw;
    flex-direction: row;
    gap: 4vw;
}

.how {
    border-radius: 1vh;
    flex: 3;
    display: flex;
    background-color: aliceblue;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    width: 24vw;
}

.how h2 {
    margin-top: 2vh;
    font-family: 'Hammersmith One', sans-serif;
    font-size: 3vW;
    font-weight: 100;
    margin-bottom: 1vh;
}

.how img {
    width: 22vw;
    height: auto;
    margin-bottom: 2vh;
    border: 0.6vh solid gray;
}

.how:hover {
    outline: 0.6vh solid yellow;
}

</style>

<div id="how">
    <h1>How does it work?</h1>
    <div id="hows">
        <div class="how">
            <h2>Sign-up</h2>
            <img src={deven} alt="Man speaking into microphone" />
        </div>
        <div class="how">
            <h2>Code together</h2>
            <img alt="Group of teenagers" src={codetogether} />
        </div>
        <div class="how">
            <h2>Get prizes</h2>
            <img alt="Teenagers with plushies on their heads" src={prizes} />
        </div>
    </div>
</div>