<script lang='ts'>
    import { onMount } from 'svelte';

    onMount(() => {
        const acc = document.getElementsByClassName("q");

        for (let i = 0; i < acc.length; i++) {
            const button = acc[i].querySelector("button") as HTMLButtonElement;
            if (button) {
                button.addEventListener("click", function(this: HTMLButtonElement) {
    this.classList.toggle("active");
    const panel = this.closest(".faq")?.querySelector(".a") as HTMLElement;
    if (!panel) return;

    const isOpen = panel.classList.toggle("open");

    panel.animate(
        [
            { height: isOpen ? "0px" : panel.scrollHeight + "px" },
            { height: isOpen ? panel.scrollHeight + "px" : "0px" },
        ],
        { duration: 350, easing: "cubic-bezier(0.4, 0, 0.2, 1)", fill: "forwards" }
    );
});
            }
        }
    });
</script>

<style>
    #section {
        display: flex;
        flex: 1;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        background-color: aliceblue;
    }

    #section h1 {
    font-family: 'Hammersmith One', sans-serif;
    font-size: 4.8vw;
    font-weight: 100;
    margin-bottom: 2vh;
    }

    .faq {
        display: flex;
        flex: 1;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        width: 70vw;
        text-align: center;
    }

    .q {
        
    }

    .q button {
    font-family: 'Hammersmith One', sans-serif;
    font-size: 2vw;
    font-weight: 100;
    margin-bottom: 2vh;
    background: none;
    background-color: rgb(246, 250, 136);
    width: 70vw;
    padding-top: 1vh;
    padding-bottom: 1vh;
    border: none;
    outline: inherit;
    cursor: pointer;
    transition: 0.4s;
    }

.a {
    overflow: hidden;
    height: 0;
    border-radius: 0 0 0.5vw 0.5vw;
}

.a.open {
    border: 0.2vw solid black;
    margin-bottom: 2vh;
}

    .a p {
    font-family: 'Hammersmith One', sans-serif;
    font-size: 1.5vw;
    font-weight: 100;
    margin-bottom: 2vh;
    }

    .a li {
    font-family: 'Hammersmith One', sans-serif;
    font-size: 1.5vw;
    font-weight: 100;
    margin-bottom: 2vh;
    }

    #listspecial {
        text-align: justify;
    }
</style>

<div id='section'>
    <h1>tell me a bit more...</h1>

    <div id="faqs">
        <div class='faq'>
            <div class='q'>
                <button>What is Sunshine?</button>
            </div>
            <div class='a'>
                <p>Sunshine is a worldwide network of free, student-led, summer coding clubs. It's all about working together, on a project. During the in-person meetup, and at home.<br/>
                    There's free food, support, stickers and prizes.<br>
                    Each week, a new challenge is released for you to hack on in a team!</p>
            </div>
        </div>
        <div class='faq'>
            <div class='q'>
                <button>How do I get prizes?</button>
            </div>
            <div class='a'>
                <p>For every hour you spend coding you get 4 Suns.<br/>
                    Meet weekly to hack on weekly challenges = get a 1.25x Sun multiplier for solving all of them.<br>
                Then, you can exchange the Suns for prizes in our shop. Prizes like, custom varsity jackets for your team, Raspberry Pis, or 3D printers!</p>
            </div>
        </div>
        <div class='faq'>
            <div class='q'>
                <button>There's no Sunshine near me!</button>
            </div>
            <div class='a'>
                <p>Host one yourself! It's really easy & super rewarding:<br></p>
                    <div id="listspecial">
                    <p>
                    
                        1. Pick a time (challenges are dropped on Mondays at 9AM EST, why not meet then?)<br>
                        2. Find a public place to meet in for at least 3 hours. Think, a café, a library, a community center.<br>
                        3. Spread the word — put up posters, invite friends, post on Facebook<br>
                        4. Get some food for the club — we'll send you $8.50 for each person that shows up!<br>
                        5. Enjoy! Lock-in with your club & work on challenges in teams!<br>
                        </p>
                        </div>
                
            </div>
        </div>
        <div class='faq'>
            <div class='q'>
                <button>Who can join?</button>
            </div>
            <div class='a'>
                <p>Anyone aged 13-18 can join Hack Club's Sunshine events!</p>
            </div>
        </div>
        
        <div class='faq'>
            <div class='q'>
                <button>How will you know how many hours I code?</button>
            </div>
            <div class='a'>
                <p>We ask you to use <a href="https://hackatime.hackclub.com">Hackatime</a>, Hack Club's add-on for tracking coding time.</p>
            </div>
            
        </div>
    </div>
</div>



<!-- 
        <div class='faq'>
            <div class='q'>
                <button></button>
            </div>
            <div class='a'>
                <p><p>
            </div>
        </div> -->