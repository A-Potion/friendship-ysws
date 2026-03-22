<script lang="ts">
let email = $state('');

function LetsRsvp() {
    let url = "https://forms.fillout.com/t/chsK1ZRiious?email=" + email;
    
    window.location.href = url;
}
</script>

<style>
    .container {
        display: inline-flex;
        gap: 0.7vw;
        align-items: center;
    }

    input {
        border-radius: 16px;
        background: #D9D9D9;
        padding: 12px 16px;
        font-size: clamp(2vw, 6vw, 2vw);
        width: clamp(26vw, calc(100vw - 120px), 22vw);
        border: 1px solid #D9D9D9;
        align-items: center;
        box-shadow: 0.2vh 0.2vh 0.5vh black;
    }

    button {
        width: clamp(45px, 18vw, 8vw);
        height: clamp(40px, 15vw, 4vw);
        border-radius: 16px;
        background: #D9D9D9;
        border: 0px solid #333;
        font-size: clamp(18px, 2.5vw, 24px);
        cursor: pointer;
        font-weight: 530;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-shrink: 0;
        box-shadow: 0.2vh 0.2vh 0.5vh black;
    }

    @media (max-width: 480px) {
        .container {
            flex-direction: column;
            gap: 10px;
        }
        input {
            width: 100%;
        }
    }
</style>


<div class="container">
    <input bind:value={email} placeholder="email">
    <button onclick={LetsRsvp}>SIGN UP</button>
</div>